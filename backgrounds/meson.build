dataconf = configuration_data()
dataconf.set('BACKGROUNDDIR', backgrounddir)
dataconf.set('datadir', datadir)

backgrounds = [
  'AcreetionOS-GNOME.jpg'
]

install_data(backgrounds, install_dir: backgrounddir)

foreach metadata : [
  'AcreetionOS-GNOME.xml']
  configure_file(
    input: metadata + '.in',
    output: metadata,
    configuration: dataconf,
    install: true,
    install_dir: metadatadir
  )
endforeach

