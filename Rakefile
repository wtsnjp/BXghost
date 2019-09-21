# Rakefile for wtsnjp/bxghost
require 'rake/clean'
require 'pathname'

# basics
PKG_NAME = "bxghost"
PKG_VERSION = "0.2.0"
PKG_FULL = "#{PKG_NAME}-#{PKG_VERSION}"

# directories
REPO_ROOT = Pathname.pwd
TMP_DIR = REPO_ROOT + "tmp"
TARGET_DIR = TMP_DIR + "#{PKG_FULL}"

# cleaning
CLEAN.include([
  "**/*.aux", "**/*.dvi", "**/*.log", "**/*.synctex.gz", "tmp"
])
CLOBBER.include(["**/*.pdf", "#{PKG_FULL}.zip"])

# deault
task default: :archive

desc "Create an archive for TeX Live"
task :archive do
  # initialize the target
  rm_rf TARGET_DIR
  mkdir_p TARGET_DIR

  # copy files to the target dir
  pkg_files = ["LICENSE", "README.md", "#{PKG_NAME}.sty"]
  cp_r pkg_files, TARGET_DIR

  # create zip archive
  cd TMP_DIR
  sh "zip -q -r #{PKG_FULL}.zip #{PKG_FULL}"
  mv "#{PKG_FULL}.zip", REPO_ROOT
end
