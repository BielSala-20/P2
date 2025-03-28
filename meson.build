project('Práctica 2 de PAV - detección de actividad vocal', 'c')

exe = 'vad'
src = ['src/main_vad.c', 'src/vad.c', 'src/pav_analysis.c']
lib = ['-lm', '-lsndfile']

inputD0 = files('src/vad.docopt')
progD0 = files('docopt_c/docopt_c.py')
outputD0 = 'vad_docopt.h'

headerD0 = custom_target('Construye vad_docopt.h',
output: outputD0, command: [progD0, inputD0, '-o', outputD0])
executable(exe, sources: [src, headerD0], link_args: lib)
