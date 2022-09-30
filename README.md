# qfilter
qfilter filters FASTQ files by PHRED quality and read length

qfilter filters FASTQ files by PHRED quality and read length. You can set a minimum (-x) and maximum (-y) required read length. You can set a minimum PHRED score (-s) EVERY nucleotide in a read must have or the minimum PHRED score that a least x percent (-p) of all nucleotides of a read must have. Then you can set the average PHRED score (-m) a read should have.
The output to STDOUT contains all matching reads (filtered). If logging (-l) is enabled, annotations are added to the identifier line. The optional logfile (-l or -lFILENAME) contains ALL reads (not filtered) with annotation in the identifier line.

Usage: qfilter  [ -h | --help ]
		            [ -p | --percent-min-phred-score PERCENT_MIN_NT_PHRED_SCORE]  	default: 100
                [ -s | --min-nt-phred-score MIN_NT_PHRED_SCORE ] 		            default: 12
                [ -m | --min-avg-phred-score MIN_AVG_PHRED_SCORE ] 		          default: 12
                [ -x | --min-read-length MIN_READ_LENGTH ] 			                default: 800
                [ -y | --max-read-length MAX_READ_LENGTH ] 			                default: 50000
		            [ -l | --log-file ][LOGFILENAME] fastqfilename(s)		            default: rwfilter.log | NO SPACE: -lLOGFILENAME
