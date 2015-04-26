require "yast/rake"

Yast::Tasks.configuration do |conf|
  # lets ignore license check for now
  conf.skip_license_check << /.*/
  conf.install_locations["doc/autodocs"] = conf.install_doc_dir
end

# FIXME: remove this, load the CI tasks directly in yast-rake
begin
  require "yast/rake_ci"
  rescue LoadError
    puts "INFO: Gem yast-rake-ci not installed, extra tasks not loaded"
end
