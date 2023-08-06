# CBT995
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)
This is still a work in progress. GitHub repos will be deleted and created during this period...
~~~~~~~~~~~~~~~~

//***FILE 995 contains a Wylbur distribution that is probably       *   FILE 995
//*           suitable to be installed on a pre-XA MVS system.      *   FILE 995
//*           The code is written to run on MVS 3.8 and MVS/SP.     *   FILE 995
//*                                                                 *   FILE 995
//*           Thanks to Bill Smith for sending this in.             *   FILE 995
//*                                                                 *   FILE 995
//*           There are two distribution files containing           *   FILE 995
//*           whole packages.  These are:                           *   FILE 995
//*                                                                 *   FILE 995
//*           WYLTSO  - GZIP AWS tape file with 14 individual       *   FILE 995
//*                     files.  To install Wylbur on MVS, and       *   FILE 995
//*                     accessory programs.                         *   FILE 995
//*                                                                 *   FILE 995
//*           WYLCMS  - GZIP AWS tape file to install Wylbur        *   FILE 995
//*                     on CMS.                                     *   FILE 995
//*                                                                 *   FILE 995
//*       I have expanded the WYLTSO tape into its 14 files,        *   FILE 995
//*       which are 14 pds'es, but I have not touched the WYLCMS    *   FILE 995
//*       tape.  Using WYLCMS is up to you......                    *   FILE 995
//*                                                                 *   FILE 995
//*       If you need help with the packaging, my email address:    *   FILE 995
//*                                                                 *   FILE 995
//*           email:   sbgolob@cbttape.org                          *   FILE 995
//*                                                                 *   FILE 995
//*       TO INSTALL FROM THE GZIP-ED AWS FILES:                    *   FILE 995
//*                                                                 *   FILE 995
//*       You need to download the GZIP AWS format files to a PC    *   FILE 995
//*       in BINARY and unzip them.  They are emulated tapes,       *   FILE 995
//*       in AWS format.  If you have a real tape drive, the        *   FILE 995
//*       VTT2TAPE program from CBT File 533 might help you to      *   FILE 995
//*       cut a real tape from this file.                           *   FILE 995
//*                                                                 *   FILE 995
//*       TO INSTALL FROM THE SEPARATE FILES: (14 files from tape)  *   FILE 995
//*                                                                 *   FILE 995
//*       The following members are OFFLOAD-ed from the tape        *   FILE 995
//*       files for WYLTSO:  Use the PDSLOAD program to get them    *   FILE 995
//*       into PDS'es.                                              *   FILE 995
//*                                                                 *   FILE 995
//*       Customize the $PDSLOAD job to conform to your site's      *   FILE 995
//*       naming conventions, and submit it.                        *   FILE 995
//*                                                                 *   FILE 995
//*       ASM                                                       *   FILE 995
//*       CNTL                                                      *   FILE 995
//*       DOCLIB                                                    *   FILE 995
//*       HELP                                                      *   FILE 995
//*       MACLIB                                                    *   FILE 995
//*       MACLIBO                                                   *   FILE 995
//*       OBJ                                                       *   FILE 995
//*       PROCS                                                     *   FILE 995
//*       SYS2HELP                                                  *   FILE 995
//*       LIB2CNTL                                                  *   FILE 995
//*       LIB2FIX                                                   *   FILE 995
//*       LIB2SRCE                                                  *   FILE 995
//*                                                                 *   FILE 995
//*       These are in FB format, LRECL=80.                         *   FILE 995
//*                                                                 *   FILE 995
//*       Then deal with the other two files:                       *   FILE 995
//*                                                                 *   FILE 995
//*       Two other files are in a VB format, but I've supplied     *   FILE 995
//*       FB-80 versions of them, just to make sure that you have   *   FILE 995
//*       the right material available in this file.                *   FILE 995
//*       The files are:                                            *   FILE 995
//*                                                                 *   FILE 995
//*       MENUS  -  Which should be VB LRECL=84    and              *   FILE 995
//*       MSGS   -  Which should be VB LRECL=76                     *   FILE 995
//*                                                                 *   FILE 995
//*       To try to get it right for you, I've packaged these 2     *   FILE 995
//*       files in TSO XMIT format, so the VB and LRECL quantities  *   FILE 995
//*       are proper, when you TSO RECEIVE them.  They are members: *   FILE 995
//*                                                                 *   FILE 995
//*       WYLMENUS  -  XMIT of the MENUS dataset                    *   FILE 995
//*       WYLMSGS   -  XMIT of the MSGS  dataset                    *   FILE 995
//*                                                                 *   FILE 995
//*       If you don't have access to TSO RECEIVE, I've FB-80-ized  *   FILE 995
//*       them, and you can copy the material into VB datasets      *   FILE 995
//*       that you allocate for yourselves.  These members are:     *   FILE 995
//*                                                                 *   FILE 995
//*       MENUSF -  FB-80 version of the MENUS library              *   FILE 995
//*       MSGSF  -  FB-80 version of the MSGS  library              *   FILE 995
//*                                                                 *   FILE 995
//*       Using these datasets, you shouldn't lose any of the       *   FILE 995
//*       material, because VB, LRECL=84 has 80 bytes of real       *   FILE 995
//*       data.  The first 4 bytes are the RDW (Record Descriptor   *   FILE 995
//*       Word).                                                    *   FILE 995
//*                                                                 *   FILE 995
//*       Then to install, follow the directions in the CNTL        *   FILE 995
//*       file to assemble and linkedit.                            *   FILE 995
//*                                                                 *   FILE 995
~~~~~~~~~~~~~~~~

