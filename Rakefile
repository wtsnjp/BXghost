# Rakefile for wtsnjp/bxghost
require 'rake/clean'
require 'pathname'

# basics
PKG_NAME = "bxghost"
PKG_VERSION = "0.5.1"
PKG_FULL = "#{PKG_NAME}-#{PKG_VERSION}"

# dir and file
BASE_DIR = Pathname.pwd
TMP_DIR = BASE_DIR / "tmp"
TARGET_DIR = TMP_DIR / PKG_NAME
ZIP_NAME = "#{PKG_NAME}-#{PKG_VERSION}.zip"

# cleaning
CLEAN.include([
  "**/*.aux", "**/*.dvi", "**/*.log", "**/*.synctex.gz", "tmp"
])
CLOBBER.include(["**/*.pdf", ZIP_NAME])

# deault
task default: :archive

desc "Create an archive for TeX Live"
task :archive do
  # initialize the target
  rm_rf TARGET_DIR
  mkdir_p TARGET_DIR

  # copy files to the target dir
  pkg_files = ["LICENSE", "README.md"] + Dir.glob("*.sty")
  cp pkg_files, TARGET_DIR

  # create zip archive
  cd TMP_DIR
  sh "zip -q -r #{ZIP_NAME} #{PKG_NAME}"
  mv ZIP_NAME, BASE_DIR
end
