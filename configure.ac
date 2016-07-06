AC_INIT(cppsp, version-0.1, private0x01@gmail.com)

if test -z $CXXFLAGS; then
    CXXFLAGS='-O2 --std=c++0x -fPIC -fwrapv -fno-delete-null-pointer-checks -funsigned-char -fno-strict-aliasing -Wno-pmf-conversions'
fi

AC_PROG_CXX
AC_LANG(C++)
AC_ARG_WITH(websocket, [  --with-websocket        Enable websocket support])

AC_SUBST(EXTRA_LIBRARIES)
AC_SUBST(EXTRA_SOURCES)

if test "$with_websocket" == "yes"
then
	AC_MSG_NOTICE([Websocket support enabled])
	AC_CHECK_HEADER(cryptopp/cryptlib.h)
	if test "$ac_cv_header_cryptopp_cryptlib_h" == no
	then
		AC_MSG_ERROR([Websocket support requires libcrypto++ to be installed])
	fi
	EXTRA_LIBRARIES+="-lcryptopp"
	EXTRA_SOURCES+="websocket.C"
fi

AC_OUTPUT(Makefile)
