cmake_minimum_required(VERSION 3.15)

set(CMAKE_EXPORT_COMPILE_COMMANDS true)

project(openssl LANGUAGES C)

set(CMAKE_C_STANDARD 99)

add_library(crypto STATIC
	crypto/asn1/a_object.c
	crypto/asn1/a_bitstr.c
	crypto/asn1/a_utctm.c
	crypto/asn1/a_gentm.c
	crypto/asn1/a_time.c
	crypto/asn1/a_int.c
	crypto/asn1/a_octet.c
	crypto/asn1/a_null.c
	crypto/asn1/a_print.c
	crypto/asn1/a_type.c
	crypto/asn1/a_set.c
	crypto/asn1/a_dup.c
	crypto/asn1/a_d2i_fp.c
	crypto/asn1/a_i2d_fp.c
	crypto/asn1/a_bmp.c
	crypto/asn1/a_enum.c
	crypto/asn1/a_vis.c
	crypto/asn1/a_utf8.c
	crypto/asn1/a_sign.c
	crypto/asn1/a_digest.c
	crypto/asn1/a_verify.c
	crypto/asn1/a_mbstr.c
	crypto/asn1/x_algor.c
	crypto/asn1/x_val.c
	crypto/asn1/x_pubkey.c
	crypto/asn1/x_sig.c
	crypto/asn1/x_req.c
	crypto/asn1/x_attrib.c
	crypto/asn1/x_name.c
	crypto/asn1/x_cinf.c
	crypto/asn1/x_x509.c
	crypto/asn1/x_x509a.c
	crypto/asn1/x_crl.c
	crypto/asn1/x_info.c
	crypto/asn1/x_spki.c
	crypto/asn1/nsseq.c
	crypto/asn1/d2i_r_pr.c
	crypto/asn1/i2d_r_pr.c
	crypto/asn1/d2i_r_pu.c
	crypto/asn1/i2d_r_pu.c
	crypto/asn1/d2i_s_pr.c
	crypto/asn1/i2d_s_pr.c
	crypto/asn1/d2i_s_pu.c
	crypto/asn1/i2d_s_pu.c
	crypto/asn1/d2i_pu.c
	crypto/asn1/d2i_pr.c
	crypto/asn1/i2d_pu.c
	crypto/asn1/i2d_pr.c
	crypto/asn1/t_req.c
	crypto/asn1/t_x509.c
	crypto/asn1/t_x509a.c
	crypto/asn1/t_crl.c
	crypto/asn1/t_pkey.c
	crypto/asn1/t_spki.c
	crypto/asn1/t_bitst.c
	crypto/asn1/p7_i_s.c
	crypto/asn1/p7_signi.c
	crypto/asn1/p7_signd.c
	crypto/asn1/p7_recip.c
	crypto/asn1/p7_enc_c.c
	crypto/asn1/p7_evp.c
	crypto/asn1/p7_dgst.c
	crypto/asn1/p7_s_e.c
	crypto/asn1/p7_enc.c
	crypto/asn1/p7_lib.c
	crypto/asn1/f_int.c
	crypto/asn1/f_string.c
	crypto/asn1/i2d_dhp.c
	crypto/asn1/i2d_dsap.c
	crypto/asn1/d2i_dhp.c
	crypto/asn1/d2i_dsap.c
	crypto/asn1/n_pkey.c
	crypto/asn1/f_enum.c
	crypto/asn1/a_hdr.c
	crypto/asn1/x_pkey.c
	crypto/asn1/a_bool.c
	crypto/asn1/x_exten.c
	crypto/asn1/asn1_par.c
	crypto/asn1/asn1_lib.c
	crypto/asn1/asn1_err.c
	crypto/asn1/a_meth.c
	crypto/asn1/a_bytes.c
	crypto/asn1/a_strnid.c
	crypto/asn1/evp_asn1.c
	crypto/asn1/asn_pack.c
	crypto/asn1/p5_pbe.c
	crypto/asn1/p5_pbev2.c
	crypto/asn1/p8_pkey.c

	crypto/bf/bf_skey.c
	crypto/bf/bf_ecb.c
	crypto/bf/bf_enc.c
	crypto/bf/bf_cfb64.c
	crypto/bf/bf_ofb64.c

	crypto/bio/bio_lib.c
	crypto/bio/bio_cb.c
	crypto/bio/bio_err.c
	crypto/bio/bss_mem.c
	crypto/bio/bss_null.c
	crypto/bio/bss_fd.c
	crypto/bio/bss_file.c
	crypto/bio/bss_sock.c
	crypto/bio/bss_conn.c
	crypto/bio/bf_null.c
	crypto/bio/bf_buff.c
	crypto/bio/b_print.c
	crypto/bio/b_dump.c
	crypto/bio/b_sock.c
	crypto/bio/bss_acpt.c
	crypto/bio/bf_nbio.c
	crypto/bio/bss_log.c
	crypto/bio/bss_bio.c

	crypto/bn/bn_add.c
	crypto/bn/bn_div.c
	crypto/bn/bn_exp.c
	crypto/bn/bn_lib.c
	crypto/bn/bn_ctx.c
	crypto/bn/bn_mul.c
	crypto/bn/bn_print.c
	crypto/bn/bn_rand.c
	crypto/bn/bn_shift.c
	crypto/bn/bn_word.c
	crypto/bn/bn_blind.c
	crypto/bn/bn_gcd.c
	crypto/bn/bn_prime.c
	crypto/bn/bn_err.c
	crypto/bn/bn_sqr.c
	crypto/bn/bn_asm.c
	crypto/bn/bn_recp.c
	crypto/bn/bn_mont.c
	crypto/bn/bn_mpi.c
	crypto/bn/bn_exp2.c

	crypto/buffer/buffer.c
	crypto/buffer/buf_err.c

	crypto/cast/c_skey.c
	crypto/cast/c_ecb.c
	crypto/cast/c_enc.c
	crypto/cast/c_cfb64.c
	crypto/cast/c_ofb64.c

	crypto/comp/comp_lib.c
	crypto/comp/c_rle.c
	crypto/comp/c_zlib.c

	crypto/conf/conf.c
	crypto/conf/conf_err.c

	crypto/des/cbc_cksm.c
	crypto/des/cbc_enc.c
	crypto/des/cfb64enc.c
	crypto/des/cfb_enc.c
	crypto/des/ecb3_enc.c
	crypto/des/ecb_enc.c
	crypto/des/enc_read.c
	crypto/des/enc_writ.c
	crypto/des/fcrypt.c
	crypto/des/ofb64enc.c
	crypto/des/ofb_enc.c
	crypto/des/pcbc_enc.c
	crypto/des/qud_cksm.c
	crypto/des/rand_key.c
	crypto/des/read_pwd.c
	crypto/des/rpc_enc.c
	crypto/des/set_key.c
	crypto/des/des_enc.c
	crypto/des/fcrypt_b.c
	crypto/des/read2pwd.c
	crypto/des/xcbc_enc.c
	crypto/des/str2key.c
	crypto/des/cfb64ede.c
	crypto/des/ofb64ede.c
	crypto/des/ede_cbcm_enc.c

	crypto/dh/dh_gen.c
	crypto/dh/dh_key.c
	crypto/dh/dh_lib.c
	crypto/dh/dh_check.c
	crypto/dh/dh_err.c

	crypto/dsa/dsa_gen.c
	crypto/dsa/dsa_key.c
	crypto/dsa/dsa_lib.c
	crypto/dsa/dsa_asn1.c
	crypto/dsa/dsa_vrf.c
	crypto/dsa/dsa_sign.c
	crypto/dsa/dsa_err.c
	crypto/dsa/dsa_ossl.c

	crypto/err/err.c
	crypto/err/err_all.c
	crypto/err/err_prn.c

	crypto/evp/encode.c
	crypto/evp/digest.c
	crypto/evp/evp_enc.c
	crypto/evp/evp_key.c
	crypto/evp/e_ecb_d.c
	crypto/evp/e_cbc_d.c
	crypto/evp/e_cfb_d.c
	crypto/evp/e_ofb_d.c
	crypto/evp/e_ecb_i.c
	crypto/evp/e_cbc_i.c
	crypto/evp/e_cfb_i.c
	crypto/evp/e_ofb_i.c
	crypto/evp/e_ecb_3d.c
	crypto/evp/e_cbc_3d.c
	crypto/evp/e_rc4.c
	crypto/evp/names.c
	crypto/evp/e_cfb_3d.c
	crypto/evp/e_ofb_3d.c
	crypto/evp/e_xcbc_d.c
	crypto/evp/e_ecb_r2.c
	crypto/evp/e_cbc_r2.c
	crypto/evp/e_cfb_r2.c
	crypto/evp/e_ofb_r2.c
	crypto/evp/e_ecb_bf.c
	crypto/evp/e_cbc_bf.c
	crypto/evp/e_cfb_bf.c
	crypto/evp/e_ofb_bf.c
	crypto/evp/e_ecb_c.c
	crypto/evp/e_cbc_c.c
	crypto/evp/e_cfb_c.c
	crypto/evp/e_ofb_c.c
	crypto/evp/e_ecb_r5.c
	crypto/evp/e_cbc_r5.c
	crypto/evp/e_cfb_r5.c
	crypto/evp/e_ofb_r5.c
	crypto/evp/m_null.c
	crypto/evp/m_md2.c
	crypto/evp/m_md5.c
	crypto/evp/m_sha.c
	crypto/evp/m_sha1.c
	crypto/evp/m_dss.c
	crypto/evp/m_dss1.c
	crypto/evp/m_mdc2.c
	crypto/evp/m_ripemd.c
	crypto/evp/p_open.c
	crypto/evp/p_seal.c
	crypto/evp/p_sign.c
	crypto/evp/p_verify.c
	crypto/evp/p_lib.c
	crypto/evp/p_enc.c
	crypto/evp/p_dec.c
	crypto/evp/bio_md.c
	crypto/evp/bio_b64.c
	crypto/evp/bio_enc.c
	crypto/evp/evp_err.c
	crypto/evp/e_null.c
	crypto/evp/c_all.c
	crypto/evp/c_allc.c
	crypto/evp/c_alld.c
	crypto/evp/evp_lib.c
	crypto/evp/bio_ok.c
	crypto/evp/evp_pkey.c
	crypto/evp/evp_pbe.c
	crypto/evp/p5_crpt.c
	crypto/evp/p5_crpt2.c

	crypto/hmac/hmac.c

	crypto/idea/i_cbc.c
	crypto/idea/i_cfb64.c
	crypto/idea/i_ofb64.c
	crypto/idea/i_ecb.c
	crypto/idea/i_skey.c

	crypto/lhash/lhash.c
	crypto/lhash/lh_stats.c

	crypto/md2/md2_dgst.c
	crypto/md2/md2_one.c

	crypto/md5/md5_dgst.c
	crypto/md5/md5_one.c

	crypto/mdc2/mdc2dgst.c
	crypto/mdc2/mdc2_one.c

	crypto/objects/o_names.c
	crypto/objects/obj_dat.c
	crypto/objects/obj_lib.c
	crypto/objects/obj_err.c

	crypto/pem/pem_sign.c
	crypto/pem/pem_seal.c
	crypto/pem/pem_info.c
	crypto/pem/pem_lib.c
	crypto/pem/pem_all.c
	crypto/pem/pem_err.c

	crypto/pkcs7/pk7_lib.c
	crypto/pkcs7/pkcs7err.c
	crypto/pkcs7/pk7_doit.c
	crypto/pkcs7/pk7_smime.c
	crypto/pkcs7/pk7_attr.c
	crypto/pkcs7/pk7_mime.c

	crypto/pkcs12/p12_add.c
	crypto/pkcs12/p12_attr.c
	crypto/pkcs12/p12_bags.c
	crypto/pkcs12/p12_crpt.c
	crypto/pkcs12/p12_crt.c
	crypto/pkcs12/p12_decr.c
	crypto/pkcs12/p12_init.c
	crypto/pkcs12/p12_key.c
	crypto/pkcs12/p12_kiss.c
	crypto/pkcs12/p12_lib.c
	crypto/pkcs12/p12_mac.c
	crypto/pkcs12/p12_mutl.c
	crypto/pkcs12/p12_sbag.c
	crypto/pkcs12/p12_utl.c
	crypto/pkcs12/p12_npas.c
	crypto/pkcs12/pk12err.c

	crypto/rand/md_rand.c
	crypto/rand/randfile.c
	crypto/rand/rand_lib.c
	crypto/rand/rand_err.c
	crypto/rand/rand_egd.c

	crypto/rc2/rc2_ecb.c
	crypto/rc2/rc2_skey.c
	crypto/rc2/rc2_cbc.c
	crypto/rc2/rc2cfb64.c
	crypto/rc2/rc2ofb64.c

	crypto/rc4/rc4_skey.c
	crypto/rc4/rc4_enc.c

	crypto/rc5/rc5_skey.c
	crypto/rc5/rc5_ecb.c
	crypto/rc5/rc5_enc.c
	crypto/rc5/rc5cfb64.c
	crypto/rc5/rc5ofb64.c

	crypto/ripemd/rmd_dgst.c
	crypto/ripemd/rmd_one.c

	crypto/rsa/rsa_eay.c
	crypto/rsa/rsa_gen.c
	crypto/rsa/rsa_lib.c
	crypto/rsa/rsa_sign.c
	crypto/rsa/rsa_saos.c
	crypto/rsa/rsa_err.c
	crypto/rsa/rsa_pk1.c
	crypto/rsa/rsa_ssl.c
	crypto/rsa/rsa_none.c
	crypto/rsa/rsa_oaep.c
	crypto/rsa/rsa_chk.c
	crypto/rsa/rsa_null.c

	crypto/sha/sha_dgst.c
	crypto/sha/sha1dgst.c
	crypto/sha/sha_one.c
	crypto/sha/sha1_one.c

	crypto/stack/stack.c

	crypto/txt_db/txt_db.c

	crypto/x509/x509_def.c
	crypto/x509/x509_d2.c
	crypto/x509/x509_r2x.c
	crypto/x509/x509_cmp.c
	crypto/x509/x509_obj.c
	crypto/x509/x509_req.c
	crypto/x509/x509spki.c
	crypto/x509/x509_vfy.c
	crypto/x509/x509_set.c
	crypto/x509/x509rset.c
	crypto/x509/x509_err.c
	crypto/x509/x509name.c
	crypto/x509/x509_v3.c
	crypto/x509/x509_ext.c
	crypto/x509/x509_att.c
	crypto/x509/x509type.c
	crypto/x509/x509_lu.c
	crypto/x509/x_all.c
	crypto/x509/x509_txt.c
	crypto/x509/x509_trs.c
	crypto/x509/by_file.c
	crypto/x509/by_dir.c

	crypto/x509v3/v3_bcons.c
	crypto/x509v3/v3_bitst.c
	crypto/x509v3/v3_conf.c
	crypto/x509v3/v3_extku.c
	crypto/x509v3/v3_ia5.c
	crypto/x509v3/v3_lib.c
	crypto/x509v3/v3_prn.c
	crypto/x509v3/v3_utl.c
	crypto/x509v3/v3err.c
	crypto/x509v3/v3_genn.c
	crypto/x509v3/v3_alt.c
	crypto/x509v3/v3_skey.c
	crypto/x509v3/v3_akey.c
	crypto/x509v3/v3_pku.c
	crypto/x509v3/v3_int.c
	crypto/x509v3/v3_enum.c
	crypto/x509v3/v3_sxnet.c
	crypto/x509v3/v3_cpols.c
	crypto/x509v3/v3_crld.c
	crypto/x509v3/v3_purp.c
	crypto/x509v3/v3_info.c

	crypto/cryptlib.c
	crypto/mem.c
	crypto/mem_dbg.c
	crypto/cversion.c
	crypto/ex_data.c
	crypto/tmdiff.c
	crypto/cpt_err.c
	crypto/ebcdic.c
)
target_compile_options(crypto PUBLIC -O3 -fomit-frame-pointer -Wall)
target_compile_definitions(crypto PUBLIC -DNO_ASM -DL_ENDIAN -DTERMIO)
target_include_directories(crypto PUBLIC include)
target_include_directories(crypto PUBLIC SYSTEM crypto)

add_library(RSAglue STATIC rsaref/rsaref.c rsaref/rsar_err.c)
target_compile_options(RSAglue PUBLIC -O3 -fomit-frame-pointer -Wall)
target_compile_definitions(RSAglue PUBLIC -DNO_ASM -DL_ENDIAN -DTERMIO)
target_include_directories(RSAglue PUBLIC include)
target_include_directories(RSAglue PUBLIC SYSTEM crypto)
target_include_directories(RSAglue PUBLIC SYSTEM rsaref)

add_library(ssl STATIC
	ssl/s2_meth.c
	ssl/s2_srvr.c
	ssl/s2_clnt.c
	ssl/s2_lib.c
	ssl/s2_enc.c
	ssl/s2_pkt.c
	ssl/s3_meth.c
	ssl/s3_srvr.c
	ssl/s3_clnt.c
	ssl/s3_lib.c
	ssl/s3_enc.c
	ssl/s3_pkt.c
	ssl/s3_both.c
	ssl/s23_meth.c
	ssl/s23_srvr.c
	ssl/s23_clnt.c
	ssl/s23_lib.c
	ssl/s23_pkt.c
	ssl/t1_meth.c
	ssl/t1_srvr.c
	ssl/t1_clnt.c
	ssl/t1_lib.c
	ssl/t1_enc.c
	ssl/ssl_lib.c
	ssl/ssl_err2.c
	ssl/ssl_cert.c
	ssl/ssl_sess.c
	ssl/ssl_ciph.c
	ssl/ssl_stat.c
	ssl/ssl_rsa.c
	ssl/ssl_asn1.c
	ssl/ssl_txt.c
	ssl/ssl_algs.c
	ssl/bio_ssl.c
	ssl/ssl_err.c
)
target_compile_options(ssl PUBLIC -O3 -fomit-frame-pointer -Wall)
target_compile_definitions(ssl PUBLIC -DNO_ASM -DL_ENDIAN -DTERMIO)
target_include_directories(ssl PUBLIC include)
target_include_directories(ssl PUBLIC SYSTEM ssl)
