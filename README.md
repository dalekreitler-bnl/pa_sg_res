pa_sg_res_cut
    by Wuxian Shi, 13 Feb 2017
    adapted to keyword arguments by H. J. Bernstein
    frame window args added by D. Kreitler

pa_sg_res_cut [-1<first_frame>]
              [-N<frame_cutoff>]
              [-R<reslow>]
              [-r<reshigh>]
              [-S<spacegroup>]
              [-i<infile>]
              [-o<outfile>]
              [-l<logfile>]
              "infile defaults to XDS_ASCII.HKL, outfile to aimless.mtz"

pa_sg_res_cut is a bash shell script wrapper for aimless and pointless, for
the downstream processing of fast_dp output. This script allows for trimming
integrated reflection files (from XDS) based on resolution and frame number,
in addition to space group assignment.

Caveat: The impact of crystal misalignment and/or unreliable indexing in the
first few frames of data collection may still be present even if those frames
are excluded from pointless/aimless. In such cases re-running fast_dp is
recommended.

Input arg variables match those of fast_dp (where overlap occurs)

pa_sg_res was renamed to pa_sg_res_cut (which can cut out frame windows)
