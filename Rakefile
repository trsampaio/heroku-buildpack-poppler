sh "cd /app/"
sh "wget http://www.freedesktop.org/software/fontconfig/release/fontconfig-2.11.94.tar.gz"
sh "tar -xf fontconfig-2.11.94.tar.gz"
sh "cd fontconfig-2.11.94"
sh "./configure"
sh "make"

sh "cd /app/"
sh "wget http://poppler.freedesktop.org/poppler-0.37.0.tar.xz"
sh "tar -xzf poppler-0.37.0.tar.xz"
sh "cd poppler-0.37.0"
sh "FONTCONFIG_LIBS=\"-L/app/fontconfig-2.11.94/src/.libs/ -lfontconfig\""
sh "FONTCONFIG_CFLAGS=\"-I/app/fontconfig-2.11.94/\""
sh "./configure"
sh "make"
sh "cd /app/vendor/poppler/bin" 
sh "cp /app/poppler-0.37.0/utils/pdf* ."
sh "cd /bin"
sh "cp /app/poppler-0.37.0/utils/pdf* ."