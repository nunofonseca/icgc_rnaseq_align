usage: star_align.py [options]

ICGC RNA-Seq alignment wrapper for STAR alignments.

Required input parameters:
```
  --genomeDir GENOMEDIR
                        Directory containing the reference genome index
                        (default: None)
  --tarFileIn TARFILEIN
                        Input file containing the sequence information
                        (default: None)

optional input parameters:
  --out OUT             Name of the output BAM file (default: out.bam)
  --workDir WORKDIR     Work directory (default: ./)
  --metaDataTab METADATATAB
                        File containing metadata for the alignment header
                        (default: None)
  --analysisID ANALYSISID
                        Analysis ID to be considered in the metadata file
                        (default: None)
  --keepJunctions       keeps the junction file as {--out}.junctions (default:
                        False)
  --useTMP USETMP       environment variable that is used as prefix for
                        temprary data (default: None)
  --weakRGcheck         only perform weak RG record check and generate generic
                        RG ID in case of a single alignment file with multiple
                        RG records present. Use with caution! (default: False)
  -h, --help            show this help message and exit (default: False)

STAR input parameters:
  --runThreadN RUNTHREADN
                        Number of threads (default: 4)
  --outFilterMultimapScoreRange OUTFILTERMULTIMAPSCORERANGE
                        outFilterMultimapScoreRange (default: 1)
  --outFilterMultimapNmax OUTFILTERMULTIMAPNMAX
                        outFilterMultimapNmax (default: 20)
  --outFilterMismatchNmax OUTFILTERMISMATCHNMAX
                        outFilterMismatchNmax (default: 10)
  --alignIntronMax ALIGNINTRONMAX
                        alignIntronMax (default: 500000)
  --alignMatesGapMax ALIGNMATESGAPMAX
                        alignMatesGapMax (default: 1000000)
  --sjdbScore SJDBSCORE
                        sjdbScore (default: 2)
  --alignSJDBoverhangMin ALIGNSJDBOVERHANGMIN
                        alignSJDBoverhangMin (default: 1)
  --genomeLoad GENOMELOAD
                        genomeLoad (default: NoSharedMemory)
  --genomeFastaFiles GENOMEFASTAFILES
                        genome sequence in fasta format to rebuild index
                        (default: None)
  --outFilterMatchNminOverLread OUTFILTERMATCHNMINOVERLREAD
                        outFilterMatchNminOverLread (default: 0.33)
  --outFilterScoreMinOverLread OUTFILTERSCOREMINOVERLREAD
                        outFilterScoreMinOverLread (default: 0.33)
  --twopass1readsN TWOPASS1READSN
                        twopass1readsN (-1 means all reads are used for
                        remapping) (default: -1)
  --sjdbOverhang SJDBOVERHANG
                        sjdbOverhang (only necessary for two-pass mode)
                        (default: 100)
  --outSAMstrandField OUTSAMSTRANDFIELD
                        outSAMstrandField (default: intronMotif)
  --outSAMattributes OUTSAMATTRIBUTES
                        outSAMattributes (default: ['NH', 'HI', 'NM', 'MD',
                        'AS', 'XS'])
  --outSAMunmapped OUTSAMUNMAPPED
                        outSAMunmapped (default: Within)
  --outSAMtype OUTSAMTYPE
                        outSAMtype (default: ['BAM', 'SortedByCoordinate'])
  --outSAMheaderHD OUTSAMHEADERHD
                        outSAMheaderHD (default: ['@HD', 'VN:1.4'])
  --outSAMattrRGline OUTSAMATTRRGLINE
                        RG attribute line submitted to outSAMattrRGline
                        (default: None)
  --outSAMattrRGfile OUTSAMATTRRGFILE
                        File containing the RG attribute line submitted to
                        outSAMattrRGline (default: None)
  --outSAMattrRGxml OUTSAMATTRRGXML
                        XML-File in TCGA format to compile RG attribute line
                        (default: None)
```