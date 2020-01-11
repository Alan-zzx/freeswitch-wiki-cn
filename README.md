# freeswitch-wiki-cn
freeswitch英文文档翻译，持续更新

1	Index  
2	[Introduction](docs\Introduction\Introduction.md)  
2.1	Understanding the Configuration Files  
2.2	Variables  
2.2.1	Global Variables  
2.3	Call Legs  
2.4	[Endpoints](docs\Introduction\Endpoints.md)  
2.5	Life Cycle of a Call  
2.6	FreeSWITCH API  
2.7	Event System  
2.7.1	Events  
2.7.2	Event headers  
2.7.3	Event Handlers  
2.7.4	Event List  
2.7.5	List of CUSTOM Events  
2.8	[Glossary](docs\Introduction\Glossary.md)  
3	Documentation Guidelines  
4	Release Process  
5	Release Notes  
5.1	FreeSWITCH 1.10.x Release notes  
5.2	FreeSWITCH 1.8.x Release notes  
5.3	FreeSWITCH 1.6.x Release notes  
6	Installation  
6.1	FreeSWITCH First Steps  
6.2	Linux  
6.2.1	Debian 10 Buster  
6.2.2	Debian 9 Stretch  
6.2.3	CentOS 7 and RHEL 7  
6.2.4	Archived Linux Installation Instructions  
6.2.4.1	CentOS 5  
6.2.4.2	CentOS 6  
6.2.4.3	CentOS 7  
6.2.4.4	Debian 7  
6.2.4.5	Debian 8 Jessie  
6.2.4.5.1	Building debs for other architectures  
6.2.4.5.2	Debian Post-Install Tasks  
6.2.4.5.3	FreeSWITCH 1.6 Video  
6.2.4.6	Fedora 29  
6.2.4.7	Git Install  
6.2.4.8	Linux Quick Install Guide  
6.2.4.9	Ubuntu  
6.2.4.10	Ubuntu 14.04 Trusty  
6.2.4.11	Ubuntu 16.04 Xenial  
6.2.4.12	Ubuntu Quick Start  
6.2.5	FreeSWITCH Repository Guide  
6.2.6	Vanilla installation files  
6.3	macOS  
6.3.1	macOS Installation  
6.3.1.1	macOS macFI Installation  
6.3.1.2	macOS Manual Installation  
6.3.2	macOS Testing and Diagnostics  
6.3.3	macOS Customization  
6.3.4	macOS 24x7 Preparation  
6.3.5	macOS Email Voicemail  
6.3.6	MacOS Archive  
6.3.6.1	Installation on OS X 10.11 El Capitan  
6.3.6.2	Installation on OS X 10.10 Yosemite  
6.3.6.3	Installation on OS X 10.9 Mavericks  
6.3.6.4	Installation on OS X 10.8 Mountain Lion  
6.3.6.5	Installation on OS X 10.7 Lion  
6.3.6.6	Installation on OS X 10.6 Snow Leopard  
6.3.6.7	Installation and Setup on OS X  
6.3.6.8	Installation on OS X Alternatives  
6.4	Unix  
6.4.1	DragonFlyBSD  
6.4.2	FreeBSD  
6.4.3	NetBSD  
6.4.4	OpenBSD  
6.4.5	Solaris  
6.5	Virtualization  
6.5.1	Amazon EC2  
6.5.2	SmartOS  
6.5.3	Virtualization Experiences  
6.6	Windows  
6.7	Gentoo  
6.7.1	ISN  
6.8	Installation ARCHIVED  
6.9	Version Stamping  
6.10	Language Files  
6.11	Raspberry Pi  
6.11.1	Raspi  
6.12	FreeSWITCH Dependencies  
6.12.1	Licensing  
7	Configuration  
7.1	Before You Start  
7.2	Reloading  
7.3	How To's  
7.3.1	Routing with directory parameters  
7.3.2	Holding Bin  
7.4	ASR  
7.5	Busy Call Retry  
7.6	Cacti  
7.7	Call Center  
7.8	CDR  
7.8.1	CDR via ESL  
7.9	Clock  
7.10	Command Line Switches  
7.11	Compiling FreeSWITCH Tips and Shortcuts  
7.12	Conceptual overview  
7.13	Configuration Recipes  
7.14	Configuring FreeSWITCH  
7.14.1	Deployment Notes  
7.14.2	Switch.conf.xml  
7.14.3	min-idle-cpu  
7.14.4	vars.xml  
7.15	Default Configuration  
7.16	Dial by name directory  
7.17	Dialing tel links with freeswitch  
7.18	DTMF  
7.19	Examples of /etc/init.d/freeswitch  
7.20	FreeSWITCH PBX Example  
7.21	FreeSWITCH Scheduler API  
7.22	FreeSWITCH XML-RPC  
7.23	Gateway prefixes  
7.24	High Availability  
7.24.1	HA keepalived  
7.25	IMT  
7.26	Music on Hold  
7.27	OpenWrt  
7.28	Performance Testing and Configurations  
7.28.1	Real-world results  
7.29	Prefix_dialing  
7.30	Proxy Media  
7.31	Reference Desk  
7.32	Running inside GNU Screen  
7.33	Sofia SIP Stack  
7.33.1	Configuring SIP  
7.33.2	External Profile  
7.33.3	Gateways Configuration  
7.33.4	Outbound_profile  
7.33.5	Sofia Configuration Files  
7.33.6	Sofia Gateway Authentication Params  
7.34	Speech Phrase Management  
7.35	SSD Tuning for Linux  
7.36	TTS  
7.37	WebRTC  
7.38	XML Basics  
7.39	XML Switch Configuration  
7.40	Queue_which_calls_extensions  
7.41	Shared Line Appearance  
7.42	SBC FreeSWITCH Configuration Example 2  
8	Verto Communicator  
9	Codecs and Media  
9.1	Audio Codecs  
9.2	Video Codecs  
9.3	Bypass Media Overview  
9.3.1	Call Forward Example  
9.4	JitterBuffer  
9.5	Early Media  
9.5.1	180 vs 183 vs Early Media  
9.6	Codec Negotiation  
9.7	Dynamic Payloads  
9.8	ZRTP  
9.9	VAD and CNG  
9.10	Category:TTS  
9.11	Voice  
9.12	Working with Sound Files  
9.13	T38 Modem  
10	Databases  
10.1	ODBC DSN  
10.1.1	Using ODBC in the core  
10.2	PostgreSQL in the core  
10.3	Lua with Database  
10.4	Lua FreeSWITCH Dbh  
10.5	FreeSWITCH Databases  
10.6	ODBC.connect  
10.7	ODBC.execute  
10.8	ODBC.getData  
10.9	ODBC.nextRow  
10.10	ODBC Example  
10.11	ODBC.query  
10.12	ODBC.close  
10.13	ODBC  
11	Networking  
11.1	Access Control List (ACL)  
11.2	ALG  
11.3	Auto Nat  
11.4	DNS  
11.5	Firewall  
11.6	General NAT example scenarios  
11.7	MWI  
11.8	NAT  
11.9	Nat stun debug irc  
11.10	NAT Traversal  
11.11	QoS  
11.12	SOHO Networking Example  
12	Security  
12.1	Certificates  
12.2	Fail2Ban  
12.3	SIP TLS  
13	Directory  
13.1	XML User Directory  
13.1.1	Contact Mapping  
13.2	LDAP Directory  
14	Dialplan  
14.1	Channel Variables  
14.2	Manipulating Channel Variables  
14.3	Variables Master List  
14.4	Loopback Endpoint  
14.5	Time of Day and Holiday Routing  
14.6	XML Dialplan  
14.6.1	Demo IVR  
14.6.2	Example Offsite phones  
14.6.2.1	Example Extension Status  
14.6.3	Handling SIP Redirect  
14.7	Call Groups  
14.8	Ring group  
14.9	Inline Dialplan  
14.10	Caller Profile Field  
14.11	Call Group intercept  
14.12	Channel States  
14.13	Call States  
14.14	Cause Code Substitution Example  
14.15	Dial Plan Action Perl Example  
14.16	_Variables (work in progress)  
14.16.1	Switch core variables  
14.16.2	CDR and accounting variables  
14.16.3	mod_sofia variables  
14.16.4	mod_dialplan_xml variables  
14.16.5	temp switch core variables  
14.16.6	mod_fifo variables  
14.16.7	Global Variable local ip v4  
14.17	Dialplan Recipes  
14.18	Default Dialplan QRF  
14.19	Dialplan FollowMe  
14.20	Freeswitch IVR Originate  
14.21	Misc Destinations  
15	Modules  
15.1	XML Modules Configuration  
15.2	mod_abstraction  
15.3	mod_amqp  
15.4	mod_amr  
15.5	mod_amr_wb  
15.6	mod_av  
15.7	mod_avmd  
15.8	mod_bert  
15.9	mod_blacklist  
15.10	mod_callcenter  
15.11	mod_cdr_csv  
15.12	mod_cdr_mongodb  
15.13	mod_cdr_pg_csv  
15.14	mod_cdr_sqlite  
15.15	mod_celt  
15.16	mod_cepstral  
15.17	mod_cidlookup  
15.18	mod_cluechoo  
15.19	mod_codec2  
15.20	mod_com_amd  
15.21	mod_com_g729  
15.22	mod_commands  
15.23	mod_conference  
15.23.1	Conference CDR  
15.24	mod_console  
15.25	mod_curl  
15.26	mod_db  
15.26.1	Function db  
15.27	mod_dialplan_asterisk  
15.27.1	Extensions.conf  
15.28	mod_dingaling  
15.29	mod_directory  
15.30	mod_distributor  
15.31	mod_dptools  
15.31.1	mod_dptools: answer  
15.31.2	mod_dptools: att_xfer  
15.31.3	mod_dptools: bgsystem  
15.31.4	mod_dptools: bind_digit_action  
15.31.5	mod_dptools: bind_meta_app  
15.31.6	mod_dptools: break  
15.31.7	mod_dptools: bridge  
15.31.7.1	Call Camping  
15.31.8	mod_dptools: bridge export  
15.31.9	mod_dptools: capture  
15.31.10	mod_dptools: chat  
15.31.11	mod_dptools: check_acl  
15.31.12	mod_dptools: clear_digit_action  
15.31.13	mod_dptools: clear_speech_cache  
15.31.14	mod_dptools: cng_plc  
15.31.15	mod_dptools: deflect  
15.31.16	mod_dptools: delay_echo  
15.31.17	mod_dptools: detect_speech  
15.31.18	mod_dptools: digit_action_set_realm  
15.31.19	mod_dptools: displace_session  
15.31.20	mod_dptools: eavesdrop  
15.31.21	mod_dptools: echo  
15.31.22	mod_dptools: endless_playback  
15.31.23	mod_dptools: eval  
15.31.24	mod_dptools: event  
15.31.25	mod_dptools: execute_extension  
15.31.26	mod_dptools: export  
15.31.27	mod_dptools: fax detect  
15.31.28	mod_dptools: file_string  
15.31.29	mod_dptools: flush dtmf  
15.31.30	mod_dptools:gentones  
15.31.30.1	Tone_stream  
15.31.30.1.1	TTML  
15.31.30.2	TGML  
15.31.30.3	Silence Stream  
15.31.31	mod_dptools:group  
15.31.32	mod_dptools: hangup  
15.31.33	mod_dptools: info  
15.31.34	mod_dptools: Inline Dialplan  
15.31.35	mod_dptools: intercept  
15.31.36	mod_dptools: IVR Menu  
15.31.37	mod_dptools: Limit  
15.31.38	mod_dptools: log  
15.31.39	mod_dptools: media_reset  
15.31.40	mod_dptools: mkdir  
15.31.41	mod_dptools: multiset  
15.31.42	mod_dptools: mutex  
15.31.43	mod_dptools: page  
15.31.44	mod_dptools: park  
15.31.45	mod_dptools: phrase  
15.31.46	mod_dptools: pickup  
15.31.47	mod_dptools: play_and_detect_speech  
15.31.48	mod_dptools: play_and_get_digits  
15.31.49	mod_dptools: playback  
15.31.50	mod_dptools: pre answer  
15.31.51	mod_dptools: presence  
15.31.52	mod_dptools: privacy  
15.31.53	mod_dptools: queue_dtmf  
15.31.54	mod_dptools: read  
15.31.55	mod_dptools: record  
15.31.56	mod_dptools: record_session  
15.31.57	mod_dptools: redirect  
15.31.58	mod_dptools: regex  
15.31.59	mod_dptools: remove_bugs  
15.31.60	mod_dptools: rename  
15.31.61	mod_dptools: respond  
15.31.62	mod_dptools: ring_ready  
15.31.63	mod_dptools: say  
15.31.64	mod_dptools: sched broadcast  
15.31.65	mod_dptools: sched cancel  
15.31.66	mod_dptools: sched hangup  
15.31.67	mod_dptools: sched transfer  
15.31.68	mod_dptools: send_info  
15.31.69	mod_dptools: send display  
15.31.70	mod_dptools: send dtmf  
15.31.71	mod_dptools: session loglevel  
15.31.72	mod_dptools: set  
15.31.73	mod_dptools: set_name  
15.31.74	mod_dptools: set audio level  
15.31.75	mod_dptools: set_global  
15.31.76	mod_dptools: set_profile_var  
15.31.77	mod_dptools: set_user  
15.31.78	mod_dptools: set zombie exec  
15.31.79	mod_dptools: sleep  
15.31.80	mod_dptools: soft_hold  
15.31.81	mod_dptools: sound_test  
15.31.82	mod_dptools: speak  
15.31.83	mod_dptools: start_dtmf  
15.31.84	mod_dptools: start_dtmf_generate  
15.31.85	mod_dptools: stop_displace_session  
15.31.86	mod_dptools: stop_dtmf  
15.31.87	mod_dptools: stop_dtmf_generate  
15.31.88	mod_dptools: stop_record_session  
15.31.89	mod_dptools: stop_tone_detect  
15.31.90	mod_dptools: strepoch  
15.31.91	mod_dptools: strftime  
15.31.92	mod_dptools: strftime_tz  
15.31.93	mod_dptools: strmicroepoch  
15.31.94	mod_dptools: system  
15.31.95	mod_dptools: three_way  
15.31.96	mod_dptools: tone_detect  
15.31.97	mod_dptools: transfer  
15.31.98	mod_dptools: unbind_meta_app  
15.31.99	mod_dptools: unset  
15.31.100	mod_dptools: verbose_events  
15.31.101	mod_dptools: wait_for_answer  
15.31.102	mod_dptools: wait_for_silence  
15.31.103	mod_dptools: loop_playback  
15.32	mod_easyroute  
15.33	mod_enum  
15.33.1	Enum.conf.xml  
15.34	mod_erlang_event  
15.34.1	IVR using mod_erlang_event  
15.35	mod_esf  
15.36	mod_esl  
15.37	mod_event_multicast  
15.37.1	Event multicast.conf.xml  
15.38	mod_event_socket  
15.38.1	Debugging Event Socket Message  
15.38.2	Making Event Socket behave like the console  
15.38.3	mod_event_socket clients  
15.39	mod_event_socket_dotnet  
15.40	mod_event_zmq  
15.41	mod_expr  
15.42	mod_fail2ban  
15.43	mod_fifo  
15.43.1	Simple call center using mod fifo  
15.44	mod_file_string  
15.45	mod_flite  
15.46	mod_format_cdr  
15.47	mod_fsk  
15.48	mod_fsv  
15.48.1	Play fsv  
15.48.2	Record FSV  
15.49	mod_g711  
15.50	mod_g723_1  
15.51	mod_g729  
15.52	mod_gsmopen  
15.53	mod_h323  
15.54	mod_ha_cluster  
15.55	mod_hash  
15.56	mod_hiredis  
15.57	mod_httapi  
15.58	mod_http_cache  
15.59	mod_iLBC  
15.60	mod_isac  
15.61	mod_janus  
15.62	mod_java  
15.63	mod_json_cdr  
15.64	mod_kazoo  
15.65	mod_ladspa  
15.66	mod_lcr  
15.67	mod_ldap  
15.68	mod_local_stream  
15.69	mod_logfile  
15.70	mod_lua  
15.70.1	Serving Configuration with Lua  
15.71	mod_managed  
15.72	mod_memcache  
15.73	mod_mongo  
15.74	mod_mp4v2  
15.75	mod_native_file  
15.76	mod_nibblebill  
15.77	mod_odbc_cdr  
15.78	mod_odbc_query  
15.79	mod_opal  
15.80	mod_opus  
15.80.1	Build libopus RPMs for CentOS 7  
15.80.2	FreeSWITCH And The Opus Audio Codec  
15.81	mod_opusfile  
15.82	mod_oreka  
15.83	mod_osp  
15.84	mod_perl  
15.84.1	Mod perl hangup hook  
15.85	mod_pocketsphinx  
15.86	mod_pocketsphinx [duplicate]  
15.87	mod_portaudio  
15.88	mod_posix_timer  
15.89	mod_python  
15.89.1	Example: directory.py  
15.89.2	Example: frontdoor.py  
15.89.3	Example Recipewizard  
15.89.4	Py_Session_collectDigits  
15.89.5	Py_Session_GetDigits  
15.89.6	Py_Session_PlayAndGetDigits  
15.89.7	Py_Session_PlayFile  
15.89.8	Py_Session_Set_TTS_Params  
15.89.9	Py_Session_SetDTMFCallback  
15.89.10	Py Session RecordFile  
15.89.11	Py Session SetHangupHook  
15.89.12	Py Session SpeakText  
15.89.13	Py Session StreamFile  
15.89.14	Py Session Transfer  
15.90	mod_rad_auth  
15.91	mod_radius_cdr  
15.92	mod_rayo  
15.93	mod_redis  
15.94	mod_rss  
15.95	mod_rtc  
15.96	mod_rtmp  
15.97	mod_ruby  
15.98	mod_sangoma_codec  
15.99	mod_say_he  
15.100	mod_shell_stream  
15.101	mod_shout  
15.102	mod_signalwire  
15.103	mod_siren  
15.104	mod_skel  
15.105	mod_skinny  
15.105.1	Skinny LDAP Schema  
15.106	mod_skypopen  
15.106.1	Skypopen Directory  
15.107	mod_sms  
15.108	mod_snapshot  
15.109	mod_sndfile  
15.110	mod_snmp  
15.110.1	FreeSWITCH OID  
15.110.2	SNMP  
15.111	mod_snom  
15.112	mod_sofia  
15.112.1	Function sofia_contact  
15.112.2	Function sofia_dig  
15.113	mod_sonar  
15.114	mod_soundtouch  
15.115	mod_spandsp  
15.115.1	T.38  
15.116	mod_speex  
15.117	mod_spy  
15.118	mod_ssml  
15.119	mod_stress  
15.120	mod_syslog  
15.121	mod_timerfd  
15.122	mod_timezone  
15.123	mod_tone_stream  
15.124	mod_translate  
15.125	mod_tts_commandline  
15.126	mod_unimrcp  
15.127	mod_v8  
15.128	mod_valet_parking  
15.129	mod_verto  
15.129.1	RESTful Verto  
15.130	mod_vlc  
15.131	mod_vmd  
15.132	mod_voicemail  
15.132.1	mod_voicemail key map  
15.132.2	Voicemail  
15.133	mod_voicemail_callpage  
15.134	mod_voicemail_ivr  
15.135	mod_watson  
15.136	mod_xml_cdr  
15.137	mod_xml_curl  
15.137.1	mod_xml_curl C++ example  
15.137.2	mod_xml_curl CGI example  
15.137.3	mod_xml_curl C sharp example  
15.137.4	mod_xml_curl PHP example  
15.137.5	mod_xml_curl Python example  
15.137.6	mod_xml_curl Ramaze/Sequel groups example  
15.137.7	mod_xml_curl Ruby directory example  
15.137.8	Ruby dialplan example  
15.138	mod_xml_diaplan  
15.139	mod_xml_radius  
15.140	mod_xml_rpc  
15.140.1	Freeswitch Portal  
15.141	mod_yaml  
16	Conference  
16.1	Conference Add Call Example  
16.2	Conference Announce Count Inline  
16.3	Conference Javascript Dialer  
16.4	confcall JS  
16.5	Example Email Conference Control  
16.6	JavaScript Conference IVR  
16.7	Lua Conference Room Management example  
16.8	Outbound Conference Calls  
17	Client and Developer Interfaces  
17.1	Command-Line Interface fs_cli  
17.2	Embedding FreeSWITCH  
17.2.1	[FreeSWITCH Softphone](docs\Client and Developer Interfaces\Embedding FreeSWITCH\FreeSWITCH Softphone.md)  
17.3	Event Socket Library  
17.3.1	Event Socket Outbound  
17.4	FreeTDM  
17.4.1	Freetdm.conf Examples  
17.4.2	FreeTDM OpenR2  
17.4.3	Tones.conf Examples  
17.5	Golang ESL  
17.6	Java ESL  
17.6.1	Java CDR Logger  
17.6.2	Java ESL Client  
17.7	JavaScript  
17.7.1	JavaScript API Reference  
17.7.1.1	Session Execute  
17.7.1.2	Run  
17.7.1.3	system  
17.7.2	JavaScript Event  
17.7.2.1	JavaScript Event Handler  
17.7.3	JS Flite  
17.7.4	Javascript Examples  
17.7.4.1	Javascript Example - AfterHoursIVR  
17.7.4.2	Javascript Example - Answering Machine  
17.7.4.3	JavaScript Example - cidspoof  
17.7.4.4	JavaScript Example - cnam  
17.7.4.5	Javascript Example - Collect Account Number  
17.7.4.6	JavaScript Example - dbIVRmenu  
17.7.4.7	Javascript Example - DISA (direct inward system access)  
17.7.4.8	Javascript Example - DTMF Callback  
17.7.4.9	Javascript Example - FollowMe  
17.7.4.10	Javascript Example - HelloWorld  
17.7.4.11	Javascript Example - Intercom  
17.7.4.12	Javascript Example - Prompt For Digits  
17.7.4.13	JavaScript Example - Say IVR Menu  
17.7.4.13.1	Javascript Example - Say IVR OfficeHours  
17.7.4.14	JavaScript Example - Session in Hangup Hook  
17.7.4.15	Javascript Example - set hook  
17.7.4.16	JavaScript Example - Test Tones  
17.7.4.17	JavaScript example - XML  
17.7.4.18	Sched hangup javascript example  
17.7.4.19	Session getVariable  
17.7.5	Session  
17.7.5.1	Session_flushDigits  
17.7.5.2	Session_generateXmlCdr  
17.7.5.3	Session_getVariable  
17.7.5.4	Session_setAutoHangup  
17.7.5.5	Session answer  
17.7.5.6	Session caller id name  
17.7.5.7	Session caller id num  
17.7.5.8	Session cause  
17.7.5.9	Session causecode  
17.7.5.10	Session collectInput  
17.7.5.11	Session destination  
17.7.5.12	Session destroy  
17.7.5.13	Session dialplan  
17.7.5.14	Session flushDigits  
17.7.5.15	Session getDigits  
17.7.5.16	Session hangup  
17.7.5.17	Session name  
17.7.5.18	Session network addr  
17.7.5.19	Session originate  
17.7.5.20	Session preAnswer  
17.7.5.21	Session ready  
17.7.5.22	Session recordFile  
17.7.5.23	Session sayPhrase  
17.7.5.24	Session setAutoHangup  
17.7.5.25	Session setHangupHook  
17.7.5.26	Session ANI2  
17.7.5.27	Session Ani  
17.7.5.28	Session setVariable  
17.7.5.29	Session speak  
17.7.5.30	Session state  
17.7.5.31	Session streamFile  
17.7.5.32	Session waitForAnswer  
17.7.6	Serving Configuration with JavaScript  
17.8	Lua API Reference  
17.8.1	Lua Install dependencies  
17.8.1.1	Installing LuaSocket  
17.8.1.2	Installing LuaSQL  
17.8.1.3	Third Party Libraries  
17.8.2	Lua examples  
17.8.2.1	Lua: send SMS via Flowroute when voicemail is received  
17.8.2.2	Lua arguments calling functions  
17.8.2.3	Lua ASR TTS Directory example  
17.8.2.4	Lua Database agent login example  
17.8.2.5	Lua Directory example  
17.8.2.6	Lua DISA Example  
17.8.2.7	Lua example Bridging two calls with retry  
17.8.2.8	Lua example Send mail when no answer  
17.8.2.9	Lua Fakecall responder example  
17.8.2.10	Lua Group Pickup example  
17.8.2.11	Lua Intercom example  
17.8.2.12	Lua IVR Menu Example  
17.8.2.13	Lua Mail Call example  
17.8.2.14	Lua Mail on NoAnswer example  
17.8.2.15	Lua MythTV alert example  
17.8.2.16	Lua Numeric Paging Example  
17.8.2.17	Lua TeleCaptcha example  
17.8.2.18	Lua Welcome IVR example  
17.8.3	Lua Toolkit Jester  
17.9	Perl ESL  
17.9.1	Example Starting A Script With Systemd  
17.9.2	Perl  
17.10	PHP ESL  
17.10.1	PHP Event Socket  
17.10.2	PHP Examples  
17.10.2.1	PHP Example - Mod XML curl  
17.10.2.2	PHP Example - Wakeup call  
17.11	Python ESL  
17.11.1	Python_SBC  
17.12	Script Language Choice  
17.13	Freeswitch GUI  
17.13.1	FS Air  
17.13.2	Fs gui  
17.14	Developer Documentation  
17.15	fs_logger.pl  
17.16	fs_rpt.pl  
17.17	Ruby ESL  
17.18	Faxlib documentation  
17.19	C# ESL  
18	Interoperability  
18.1	Caller ID Privacy  
18.2	Gateways  
18.2.1	AudioCodes Gateways  
18.2.1.1	Configuring Audiocodes Behind NAT  
18.2.1.2	Configuring AudioCodes MP-114/118  
18.2.1.3	Faxlib.jm  
18.2.1.4	Fax on AudioCodes Mediant  
18.2.2	Gateway Dinstar  
18.2.3	Dinstar GSM gateway FreeSwitch HowTo  
18.2.4	Configuration OpenZAP - DigiumTDM400P Example  
18.2.4.1	Openzap Configuration Examples  
18.2.5	Gateways Other  
18.2.6	Goip HowTo  
18.2.7	Media5  
18.2.8	Obihai  
18.2.9	Pluscom  
18.2.10	Redfone  
18.3	Internet Service Provider  
18.4	NDLB  
18.5	Phone Bugs  
18.6	Phones  
18.6.1	2n  
18.6.2	Aastra  
18.6.2.1	Aastra XML  
18.6.3	ACN  
18.6.4	AudioCodes Phones  
18.6.5	Avaya  
18.6.6	AVM  
18.6.7	Cisco  
18.6.7.1	Cisco 7960 SIP  
18.6.7.2	Cisco Sample XML Config  
18.6.7.3	Cisco SPA5XX  
18.6.7.4	Cisco UC520 HowTo  
18.6.7.5	Intercom  
18.6.8	D-Link  
18.6.9	DUALPhone  
18.6.10	Grandstream  
18.6.11	Linksys  
18.6.11.1	SPA400 HowTo  
18.6.11.2	SPA2102 HowTo  
18.6.11.3	SPA3102 HowTo  
18.6.12	Mitel  
18.6.13	Mobile and Wifi  
18.6.14	Nortel  
18.6.15	Panasonic  
18.6.16	PerfecTone  
18.6.17	Polycom  
18.6.17.1	Polycom Configuration  
18.6.17.2	Polycom Corporate Directory  
18.6.17.3	Polycom Internal Ring  
18.6.17.4	Polycom Presence Setup  
18.6.17.5	Polycom Reset Codes  
18.6.18	Siemens  
18.6.19	Snom  
18.6.20	Thomson  
18.6.21	UMEC  
18.6.22	Worldgate  
18.6.23	Yealink-SIP-T26P  
18.6.24	Nokia N95  
18.6.24.1	Nokia_N95_Settings  
18.7	Providers ITSPs  
18.7.1	Provider SignalWire (US)  
18.7.2	Provider AQL (UK)  
18.7.3	Provider Bandwidth (USA)  
18.7.4	Provider BBTel (Argentina)  
18.7.5	Provider Belcentrale (Netherlands)  
18.7.6	Provider Brastel (Japan & Brazil)  
18.7.7	Provider Broadvoice (USA)  
18.7.8	Provider Broadvox (USA)  
18.7.9	Provider Budgetphone (Netherlands)  
18.7.10	Provider Callcentric (USA)  
18.7.11	Provider CallWithUs (USA)  
18.7.12	Provider cheapnet (Italy)  
18.7.13	Provider DIDforSale (US, Canada, UK)  
18.7.14	Provider DIDLogic (Global)  
18.7.15	Provider dus.net (Germany & Global)  
18.7.16	Provider equada (Germany)  
18.7.17	Provider Flowroute (USA)  
18.7.18	Provider FŌNSWITCH (USA)  
18.7.19	Provider FPT Telecom (Vietnam)  
18.7.20	Provider Freephoneline (Canada)  
18.7.21	Provider Gafachi (USA)  
18.7.22	Provider Gradwell (UK)  
18.7.23	Provider Halonet (Poland)  
18.7.24	Provider iCall (USA)  
18.7.25	Provider iinet (Australia)  
18.7.26	Provider InPhonex (USA Brazil Mexico)  
18.7.27	Provider Internode (Australia)  
18.7.28	Provider internode NodePhone (Australia)  
18.7.29	Provider internode OneSuite (USA & Canada)  
18.7.30	Provider IPKall (USA)  
18.7.31	Provider iplink (Norway)  
18.7.32	Provider ippi (France)  
18.7.33	Provider iptel (Germany & Global)  
18.7.34	Provider Iristel (Canada)  
18.7.35	Provider ivox (Australia)  
18.7.36	Provider Junctionnetworks (USA)  
18.7.37	Provider LES.NET (Canada)  
18.7.38	Provider Level3 (USA)  
18.7.39	Provider Localphone (UK)  
18.7.40	Provider MyDivert.com (Ireland)  
18.7.41	Provider MyNetFone (Australia)  
18.7.42	Provider Neotel (South Africa)  
18.7.43	Provider NetSIP (Australia)  
18.7.44	Provider netvoip.ch (Switzerland)  
18.7.45	Provider Nexmo  
18.7.46	Provider Nextiva (USA)  
18.7.47	Provider nexVortex (USA)  
18.7.48	Provider NumberGroup (UK)  
18.7.49	Provider OVH Telecom (France)  
18.7.50	Provider PennyTel (Australia)  
18.7.51	Provider PeopleLine (Canada)  
18.7.52	Provider Personal-VOIP (Germany)  
18.7.53	Provider Phonzo(Norway)  
18.7.54	Provider QXIP (Netherlands)  
18.7.55	Provider Rapidvox (USA)  
18.7.56	Provider sipcall.ch (Switzerland)  
18.7.57	Provider SipGate.de (Germany)  
18.7.58	Provider SIPRoutes (USA)  
18.7.59	Provider SipStation (USA)  
18.7.60	Provider SUREVoip (UK)  
18.7.61	Provider Telasip (USA)  
18.7.62	Provider Telegate (Australia)  
18.7.63	Provider Teliax (USA)  
18.7.64	Provider ThinkTel (Canada)  
18.7.65	Provider Tricom (Dominican Republic)  
18.7.66	Provider Twilio (US)  
18.7.67	Provider Unlimitel (Canada)  
18.7.68	Provider ViaTalk (USA)  
18.7.69	Provider Vitelity (USA)  
18.7.70	Provider VoiceNetwork (Canada)  
18.7.71	Provider VoicePulse (USA)  
18.7.71.1	Voicepulse.xml  
18.7.72	Provider voip.ms Swiftvox (USA)  
18.7.73	Provider VoipCheap (Luxembourg & Global)  
18.7.74	Provider Voip Innovations (USA)  
18.7.75	Provider VoipMeUp (Canada & USA)  
18.7.76	Provider VoIPstreet (USA)  
18.7.77	Provider VoIPtalk (UK)  
18.7.78	Provider VONAGE (USA)  
18.7.79	Provider Vono (Portugal)  
18.7.80	Provider VOXOX (USA)  
18.7.81	Provider WhistlePhone (USA)  
18.7.82	Provider XO Communications (USA)  
18.7.83	Provider Xpander Communications (USA)  
18.8	OpenZap  
18.8.1	OpenZap Dahdi  
18.8.2	OpenZap Rhino  
18.8.3	Openzap.conf Examples  
18.8.4	Openzap.conf.xml Examples  
18.8.5	Openzap.sangoma.libpri  
18.8.6	Zapata zaptel  
18.8.6.1	Zapata zaptel interface  
18.8.6.2	Zaptel B410P  
18.8.6.3	Zaptel Tutorial  
18.9	Khomp  
18.9.1	Khomp/Bridge application parameters  
18.9.2	Khomp/Commands  
18.9.3	Khomp/Contexts  
18.9.4	Khomp/Description of Variables  
18.9.5	Khomp/Error Codes  
18.9.6	Khomp/README  
18.9.7	Khomp/Settings  
18.9.8	Khomp/Variables  
18.10	Routers  
18.11	Softphones  
18.11.1	FSClient  
18.11.2	FSComm  
18.12	Software Interfaces  
18.12.1	Asterisk  
18.12.1.1	Convert Asterisk Dialplans to FreeSWITCH  
18.12.1.1.1	Converting Asterisk to FreeSWITCH  
18.12.1.2	Rosetta Stone  
18.12.2	Connecting with Nortel  
18.12.3	Microsoft Exchange UM  
18.12.4	PBX Software  
18.12.5	Skype  
18.12.5.1	Skype Connect  
18.12.5.2	SipTheeSkype Skype Adapter  
18.12.6	Telco Softswitches  
18.12.7	PBXMate  
18.13	Sangoma A200  
18.14	OpenBTS  
19	IVR  
20	Signalling  
20.1	ISDN: Integrated Services Digital Network  
20.2	MGCP  
20.3	RTCP  
20.4	UniMRCP  
20.5	RTP payload list  
20.6	RTMP Configuration Files  
20.7	ARCHIVE_Sip_execute_on_image  
21	Troubleshooting Debugging  
21.1	Debugging  
21.2	Troubleshooting Freeswitch  
21.3	Common Errors  
21.4	Debugger  
21.5	Debugging Freeswitch  
21.6	Hangup Cause Code Table  
21.7	Logging  
21.8	Packet Capture  
21.8.1	VoIPmonitor  
21.8.2	Wireshark How To  
21.9	Reporting Bugs to JIRA  
21.10	JIRA in Command Line  
21.11	RTP Issues  
21.12	SIP Protocol Messages  
21.13	Test Numbers  
21.14	Creating a freeswitch.log pastebin  
21.15	Energy Levels, Silence Thresholds, Silence Hits  
22	Community  
22.1	Authors  
22.2	Contributing Code  
22.2.1	Adopt A Module  
22.2.2	Bounty  
22.2.2.1	Bounties Completed  
22.2.3	Coding Guidelines  
22.2.4	Commit Message Guidelines  
22.2.5	Creating RPM repository  
22.2.6	Developers  
22.2.7	GSoC  
22.2.8	Janitorial Tasks  
22.2.9	Creating New Modules  
22.2.9.1	Creating a New Endpoint: Lifecycle of a Session  
22.2.9.2	Developer Potpourri  
22.2.10	Pull Requests  
22.2.11	Tips For Using Git  
22.3	Contributing Documentation  
22.3.1	Docs Team  
22.3.2	Confluence Wiki Standards and Guidelines  
22.3.3	Move Tracker  
22.3.4	Wiki Migration  
22.4	ClueCon Weekly Conference call  
22.5	Using the Mailing List  
22.6	IRC  
22.7	FreeSWITCH In The News  
22.8	Book  
23	Examples  
23.1	Playing recording external media  
23.2	AutoProvisioning and Dynamic Directories  
23.3	Caller ID LDAP Lookup  
23.4	Detect Active Channels  
23.5	Email2callback  
23.6	ENUM Caller ID lookup  
23.7	Force transfer context example  
23.8	Ham Radio  
23.9	Home PBX Example  
23.10	IVR in Perl  
23.11	mod_perl examples by Mitch Capper  
23.12	Multi-line rollover  
23.13	No-Media Mode (SDP pass through) Example  
23.14	Originate Example  
23.15	Regular Expression  
23.15.1	Sample Regexes  
23.16	Simple Call Forward with IVR  
23.17	Simple Day Nite Mode  
23.18	Simple IVR in JavaScript  
23.19	Multi-tenant  
23.20	Examples spoof py  
23.21	Advanced SBC with mod_lcr and mod_easyroute  
23.22	Example Hangup hook  
23.23	Park & Retrieve  
23.24	PRESENCE IN event example  
23.25	Presence  
23.25.1	Variable presence data cols  
23.26	mod_lcr parse scripts  
23.27	YAC  

