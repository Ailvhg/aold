<؟ php
// 𝐖𝐄𝐋𝐂𝐎𝐌𝐄 𝐓𝐎 𝐓𝐇𝐄 𝐅𝐈𝐒𝐇𝐈𝐍𝐆 𝐀𝐂𝐂𝐎𝐔𝐍𝐓𝐒 𝐏𝐑𝐎𝐆𝐑𝐀𝐌𝐌𝐄𝐃 𝐁𝐘 @ E_5_OIIQQTQ كسم يلي بغير حرف واحد كسخت يلعب بالملف أو ياخد اتصالات أو يسحب اي شي اذا ما بيك شرف غير ✌️😂 //
date_default_timezone_set ("آسيا / بغداد") ؛
إذا (! file_exists ('config.json')) {
	$ token = readline ('Enter Token:') ؛
	$ id = readline ('أدخل المعرّف:') ؛
	file_put_contents ('config.json'، json_encode (['id' => $ id، 'token' => $ token])) ؛
	
} آخر {
		  $ config = json_decode (file_get_contents ('config.json')، 1) ؛
	$ token = $ config ['token'] ؛
	$ id = $ config ['id'] ؛
}

إذا (! file_exists ('accounts.json')) {
    file_put_contents ('accounts.json'، json_encode ([])) ؛
}
تشمل "index.php" ؛
يحاول {
	رد الاتصال بالدولار = الوظيفة ($ update، $ bot) {
		معرّف $ العالمي ؛
		إذا ($ update! = null) {
		  $ config = json_decode (file_get_contents ('config.json')، 1) ؛
		  $ config ['filter'] = $ config ['filter']! = فارغ؟ $ config ['مرشح']: 1؛
      حسابات $ = json_decode (file_get_contents ('accounts.json')، 1) ؛
			إذا (isset ($ update-> message)) {
				$ message = $ update-> message؛
				$ chatId = $ message-> chat-> id ؛
				$ text = $ message-> text ؛
				إذا ($ chatId == $ id) {
					إذا ($ text == '/ haa') {
              $ bot-> sendMessage ([
                  'chat_id' => $ chatId ،
                  'text' => "- - HELLO ACTIVATION BY HAA🍯
 ↯ تيلي. ↯CH↯
 : - @ E_5_O: -IIQQTQ. "،
                  'reply_markup' => json_encode ([
                      "inline_keyboard" => [
                          [['text' => '- إضافة حساب.'، 'callback_data' => 'تسجيل الدخول']]،
                          [['text' => '- Grab Settings.'، 'callback_data' => 'grabber']] ،
                          [['text' => '- بدء الفحص.'، 'callback_data' => 'run']، ['text' => '- Stop Check.'، 'callback_data' => 'stop']]،
						  [['text' => '- حالة الأداة.'، 'callback_data' => 'status']]،
						  [['text' => '- 𝙳𝚎𝚟𝚎𝚕𝚘𝚙𝚎𝚛 𝚌𝚑𝚊𝚗𝚗𝚎𝚕 𝄋.'، 'url' => 'T.me/E_5_O']] ،
                      ]
                  ])
              ]) ؛   
          } elseif ($ text! = null) {
          	إذا ($ config ['mode']! = null) {
          		$ mode = $ config ['mode'] ؛
          		إذا (الوضع $ == 'addL') {
          			$ ig = ig جديد (['file' => ''، 'account' => ['useragent' => 'Instagram 27.0.0.7.97 Android (23 / 6.0.1؛ 640dpi؛ 1440x2392؛ LGE / lge؛ RS988 ؛ h1؛ h1؛ en_US) ']])؛
          			list ($ user، $ pass) = explode (':'، $ text)؛
          			list ($ headers، $ body) = $ ig-> تسجيل الدخول ($ user، $ pass)؛
          			// echo $ body؛
          			$ body = json_decode ($ body) ؛
          			إذا (isset ($ body-> message)) {
          				إذا (body-> message == 'Challenge_required') {
          					$ bot-> sendMessage ([
          							'chat_id' => $ chatId ،
          							'parse_mode' => 'تخفيض السعر' ،
          							'text' => "- خطأ. \ n- التحدي مطلوب."
          					]) ؛
          				} آخر {
          					$ bot-> sendMessage ([
          							'chat_id' => $ chatId ،
          							'parse_mode' => 'تخفيض السعر' ،
          							'text' => "- خطأ. \ n- اسم مستخدم أو كلمة مرور غير صحيحة."
          					]) ؛
          				}
          			} elseif (isset ($ body-> logged_in_user)) {
          				$ body = $ body-> logged_in_user؛
          				preg_match_all ('/ ^ Set-Cookie: \ s * ([^؛] *) / mi'، $ headers، $ match)؛
								  $ CookieStr = ""؛
								  foreach ($ يتطابق [1] مع $ item) {
								      $ CookieStr. = $ item. "؛"؛
								  }
          				$ account = ['cookies' => $ CookieStr، 'useragent' => 'Instagram 27.0.0.7.97 Android (23 / 6.0.1؛ 640dpi؛ 1440x2392؛ LGE / lge؛ RS988؛ h1؛ h1؛ en_US)'] ؛
          				
          				حسابات $ [$ text] = حساب $؛
          				file_put_contents ('accounts.json'، json_encode (حسابات $)) ؛
          				$ mid = $ config ['mid'] ؛
          				$ bot-> sendMessage ([
          				      'parse_mode' => 'تخفيض السعر' ،
          							'chat_id' => $ chatId ،
          							'text' => "- تم تسجيل الدخول مع @ $ user. \ n- أرسل / ابدأ لبدء التحقق."،
												'reply_to_message_id' => $ mid		
          					]) ؛
          				لوحة المفاتيح $ = ['inline_keyboard' => [
										[['text' => "- إضافة حساب جديد."، 'callback_data' => 'addL']]
									]] ؛
		              foreach (حسابات $ كـ $ account => $ v) {
		                  $ keyboard ['inline_keyboard'] [] = [['text' => $ account، 'callback_data' => 'ddd']، ['text' => "- LogOut."، 'callback_data' => 'del &' . حساب $]] ؛
		              }
		              $ keyboard ['inline_keyboard'] [] = [['text' => '- Back'، 'callback_data' => 'back']]؛
		              $ bot-> editMessageText ([
		                  'chat_id' => $ chatId ،
		                  'message_id' => متوسط ​​دولار ،
		                  'text' => "- التحكم في الحسابات."،
		                  'reply_markup' => json_encode (لوحة المفاتيح $)
		              ]) ؛
		              $ config ['mode'] = null؛
		              $ config ['mid'] = فارغ ؛
		              file_put_contents ('config.json'، json_encode ($ config)) ؛
          			}
          		} elseif ($ mode == 'selectFollowers') {
          		  إذا (is_numeric ($ text)) {
          		    bot ("sendMessage" ، [
          		        'chat_id' => $ chatId ،
          		        'text' => "- تم التعديل."،
          		        'reply_to_message_id' => $ config ['mid']
          		    ]) ؛
          		    $ config ['filter'] = $ text؛
          		    $ bot-> تحرير نص الرسالة ([
                      'chat_id' => $ chatId ،
                      'message_id' => متوسط ​​دولار ،
                     'text' => "- 𝐖𝐄𝐋𝐂𝐎𝐌𝐄 𝐓𝐎 𝐓𝐇𝐄 𝐅𝐈𝐒𝐇𝐈𝐍𝐆 𝐓𝐎𝐎𝐋 𝐀𝐂𝐂𝐎𝐔𝐍𝐓𝐒
𝐏𝐑𝐎𝐆𝐑𝐀𝐌𝐌𝐄𝐃 𝐁𝐘 @ E_5_O. "،
                  'reply_markup' => json_encode ([
                      "inline_keyboard" => [
                          [['text' => '- إضافة حساب.'، 'callback_data' => 'تسجيل الدخول']]،
                          [['text' => '- Grab Settings.'، 'callback_data' => 'grabber']] ،
                          [['text' => '- بدء الفحص.'، 'callback_data' => 'run']، ['text' => '- Stop Check.'، 'callback_data' => 'stop']]،
						  [['text' => '- حالة الأداة.'، 'callback_data' => 'status']]،
						  [['text' => '- 𝙳𝚎𝚟𝚎𝚕𝚘𝚙𝚎𝚛 𝚌𝚑𝚊𝚗𝚗𝚎𝚕 𝄋.'، 'url' => 'T.me/IIQQTQ']] ،
                      ]
                  ])
                  ]) ؛
          		    $ config ['mode'] = null؛
		              $ config ['mid'] = فارغ ؛
		              file_put_contents ('config.json'، json_encode ($ config)) ؛
          		  } آخر {
          		    bot ("sendMessage" ، [
          		        'chat_id' => $ chatId ،
          		        'text' => '- أرسل الرقم Plz ..'
          		    ]) ؛
          		  }
          		} آخر {
          		  التبديل ($ config ['mode']) {
          		    "بحث" حالة:
          		      $ config ['mode'] = null؛
          		      $ config ['Words'] = $ text؛
          		      file_put_contents ('config.json'، json_encode ($ config)) ؛
          		      exec ('screen -dmS gr php search.php') ؛
          		      فترة راحة؛
          		      حالة "المتابعين":
          		      $ config ['mode'] = null؛
          		      $ config ['Words'] = $ text؛
          		      file_put_contents ('config.json'، json_encode ($ config)) ؛
          		      exec ('screen -dmS gr php Followers.php') ؛
          		      فترة راحة؛
          		      الحالة "التالية": 
          		      $ config ['mode'] = null؛
          		      $ config ['Words'] = $ text؛
          		      file_put_contents ('config.json'، json_encode ($ config)) ؛
          		      exec ('screen -dmS gr php following.php') ؛
          		      فترة راحة؛
          		      حالة "هاشتاج": 
          		      $ config ['mode'] = null؛
          		      $ config ['Words'] = $ text؛
          		      file_put_contents ('config.json'، json_encode ($ config)) ؛
          		      exec ('screen -dmS gr php hashtag.php') ؛
          		      فترة راحة؛
          		  }
          		}
          	}
          }
				} آخر {
					$ bot-> sendMessage ([
							'chat_id' => $ chatId ،
							'text' => "- روبوت مدفوع 💲 ليس مجاني يرجى الاتصال بالمطور للحصول على معلومات إضافية."،
							'reply_markup' => json_encode ([
                  "inline_keyboard" => [
                      [['text' => '- 𝙳𝚎𝚟𝚎𝚕𝚘𝚙𝚎𝚛 𝚌𝚑𝚊𝚗𝚗𝚎𝚕 𝄋.'، 'url' => 'T.me/IIQQTQ']]
                  ]
							])
					]) ؛
				}
			} elseif (isset ($ update-> callback_query)) {
          $ chatId = $ update-> callback_query-> message-> chat-> id ؛
          $ mid = تحديث $-> callback_query-> message-> message_id ؛
          $ data = تحديث $-> callback_query-> data ؛
          صدى البيانات $؛
          إذا ($ data == 'login') {
              
        		لوحة المفاتيح $ = ['inline_keyboard' => [
										[['text' => "- إضافة حساب جديد."، 'callback_data' => 'addL']]
									]] ؛
		              foreach (حسابات $ كـ $ account => $ v) {
		                  $ keyboard ['inline_keyboard'] [] = [['text' => $ account، 'callback_data' => 'ddd']، ['text' => "- LogOut."، 'callback_data' => 'del &' . حساب $]] ؛
		              }
		              $ keyboard ['inline_keyboard'] [] = [['text' => '- رجوع.'، 'callback_data' => 'back']]؛
		              $ bot-> editMessageText ([
		                  'chat_id' => $ chatId ،
		                  'message_id' => متوسط ​​دولار ،
		                  'text' => "- التحكم في الحسابات."،
		                  'reply_markup' => json_encode (لوحة المفاتيح $)
		              ]) ؛
          } elseif ($ data == 'addL') {
          	
          	$ config ['mode'] = 'addL'؛
          	$ config ['mid'] = $ mid؛
          	file_put_contents ('config.json'، json_encode ($ config)) ؛
          	$ bot-> sendMessage ([
          			'chat_id' => $ chatId ،
          			'text' => "- حسنًا ، الآن أرسل لي الحساب. \ n- مثال => المستخدم: تمرير."،
          			'parse_mode' => 'تخفيض السعر'
          	]) ؛
          } elseif ($ data == 'grabber') {
            
            $ for = $ config ['for']! = فارغ؟ $ config ['for']: '- NoT Found'؛
            $ count = count (explode ("\ n"، file_get_contents ($ for)))؛
            $ bot-> تحرير نص الرسالة ([
                'chat_id' => $ chatId ،
                'message_id' => متوسط ​​دولار ،
                'text' => "- قائمة المستخدمين. \ n- عدد المستخدمين => $ count. \ n- الحساب قيد الاستخدام => $ for."،
                'reply_markup' => json_encode ([
                    "inline_keyboard" => [
                        [['text' => '- من البحث.'، 'callback_data' => 'بحث']]،
                        [['text' => '- From Hashtag (#).'، 'callback_data' => 'hashtag']، ['text' => '- From Explore.'، 'callback_data' => 'Explore']] و
                        [['text' => '- From Followers.'، 'callback_data' => 'Followers']، ['text' => "- From Follow."، 'callback_data' => 'follow']]،
                        [['text' => "- الحساب قيد الاستخدام: $ مقابل."، 'callback_data' => 'for']]،
                        [['text' => '- إزالة كل المستخدمين.'، 'callback_data' => 'newList']، ['text' => '- Up To Old List.'، 'callback_data' => 'إلحاق']] و
						[['text' => '- رجوع.'، 'callback_data' => 'back']]،
						[['text' => '- 𝙳𝚎𝚟𝚎𝚕𝚘𝚙𝚎𝚛 𝚌𝚑𝚊𝚗𝚗𝚎𝚕 𝄋.'، 'url' => 'T.me/IIQQTQ']] ،
                    ]
                ])
            ]) ؛
          } elseif ($ data == 'search') {
            $ bot-> sendMessage ([
                'chat_id' => $ chatId ،
                'text' => "- أرسل لي الكلمات الآن."
            ]) ؛
            $ config ['mode'] = 'بحث'؛
            file_put_contents ('config.json'، json_encode ($ config)) ؛
          } elseif ($ data == 'Followers') {
            $ bot-> sendMessage ([
                'chat_id' => $ chatId ،
                'text' => "- أرسل لي المستخدم الآن."
            ]) ؛
            $ config ['mode'] = 'المتابعون'؛
            file_put_contents ('config.json'، json_encode ($ config)) ؛
          } elseif ($ data == 'متابعة') {
            $ bot-> sendMessage ([
                'chat_id' => $ chatId ،
                'text' => "- أرسل لي المستخدم الآن."
            ]) ؛
            $ config ['mode'] = 'متابع'؛
            file_put_contents ('config.json'، json_encode ($ config)) ؛
          } elseif ($ data == 'hashtag') {
            $ bot-> sendMessage ([
                'chat_id' => $ chatId ،
                'text' => "- أرسل لي الهاشتاغ الآن (بدون #)."
            ]) ؛
            $ config ['mode'] = 'hashtag'؛
            file_put_contents ('config.json'، json_encode ($ config)) ؛
          } elseif ($ data == 'newList') {
            file_put_contents ('a'، 'new')؛
            $ bot-> answerCallbackQuery ([
							'callback_query_id' => تحديث $-> callback_query-> id ،
							'text' => "- تم."،
							"show_alert" => 1
						]) ؛
          } elseif ($ data == 'append') { 
            file_put_contents ('a'، 'ap') ؛
            $ bot-> answerCallbackQuery ([
							'callback_query_id' => تحديث $-> callback_query-> id ،
							'text' => "- تم."،
							"show_alert" => 1
						]) ؛
						
          } elseif ($ data == 'for') {
            إذا (! فارغة (حسابات $)) {
            لوحة المفاتيح $ = [] ؛
             foreach (حسابات $ كـ $ account => $ v) {
                $ keyboard ['inline_keyboard'] [] = [['text' => $ account، 'callback_data' => 'Forg &'. $ account]]؛
              }
              $ bot-> editMessageText ([
                  'chat_id' => $ chatId ،
                  'message_id' => متوسط ​​دولار ،
                  'text' => "- اختر الحساب."،
                  'reply_markup' => json_encode (لوحة المفاتيح $)
              ]) ؛
            } آخر {
              $ bot-> answerCallbackQuery ([
							'callback_query_id' => تحديث $-> callback_query-> id ،
							'text' => "- أنت لا تضيف أي حساب."،
							"show_alert" => 1
						]) ؛
            }
          } elseif ($ data == 'selectFollowers') {
            bot ("sendMessage" ، [
                'chat_id' => $ chatId ،
                'text' => '- إرسال عدد المتابعين.'  
            ]) ؛
            $ config ['mode'] = 'selectFollowers'؛
          	$ config ['mid'] = $ mid؛
          	file_put_contents ('config.json'، json_encode ($ config)) ؛
          } elseif ($ data == 'run') {
            إذا (! فارغة (حسابات $)) {
            لوحة المفاتيح $ = [] ؛
             foreach (حسابات $ كـ $ account => $ v) {
                $ keyboard ['inline_keyboard'] [] = [['text' => $ account، 'callback_data' => 'start &'. $ account]]؛
              }
              $ bot-> editMessageText ([
                  'chat_id' => $ chatId ،
                  'message_id' => متوسط ​​دولار ،
                  'text' => "- اختر الحساب."،
                  'reply_markup' => json_encode (لوحة المفاتيح $)
              ]) ؛
            } آخر {
              $ bot-> answerCallbackQuery ([
							'callback_query_id' => تحديث $-> callback_query-> id ،
							'text' => "- أنت لا تضيف أي حساب."،
							"show_alert" => 1
						]) ؛
            }
          } elseif ($ data == 'stop') {
            إذا (! فارغة (حسابات $)) {
            لوحة المفاتيح $ = [] ؛
             foreach (حسابات $ كـ $ account => $ v) {
                $ keyboard ['inline_keyboard'] [] = [['text' => $ account، 'callback_data' => 'stop &'. $ account]]؛
              }
              $ bot-> editMessageText ([
                  'chat_id' => $ chatId ،
                  'message_id' => متوسط ​​دولار ،
                  'text' => "- اختر الحساب."،
                  'reply_markup' => json_encode (لوحة المفاتيح $)
              ]) ؛
            } آخر {
              $ bot-> answerCallbackQuery ([
							'callback_query_id' => تحديث $-> callback_query-> id ،
							'text' => "- أنت لا تضيف أي حساب."،
							"show_alert" => 1
						]) ؛
            }
          } elseif ($ data == 'stopgr') {
            shell_exec ('screen -S gr -X quit') ؛
            $ bot-> answerCallbackQuery ([
							'callback_query_id' => تحديث $-> callback_query-> id ،
							'text' => "- تم التوقف."،
						// 'show_alert' => 1
						]) ؛
						$ for = $ config ['for']! = فارغ؟ $ config ['for']: 'Select Account'؛
            $ count = count (explode ("\ n"، file_get_contents ($ for)))؛
						$ bot-> editMessageText ([
                'chat_id' => $ chatId ،
                'message_id' => متوسط ​​دولار ،
                 'text' => "- قائمة المستخدمين. \ n- عدد المستخدمين => $ count. \ n- الحساب قيد الاستخدام => $ for."،
                'reply_markup' => json_encode ([
                    "inline_keyboard" => [
                        [['text' => '- من البحث.'، 'callback_data' => 'بحث']]،
                        [['text' => '- From Hashtag (#).'، 'callback_data' => 'hashtag']، ['text' => '- From Explore.'، 'callback_data' => 'Explore']] و
                        [['text' => '- From Followers.'، 'callback_data' => 'Followers']، ['text' => "- From Follow."، 'callback_data' => 'follow']]،
                        [['text' => "- الحساب قيد الاستخدام: $ مقابل."، 'callback_data' => 'for']]،
                        [['text' => '- إزالة كل المستخدمين.'، 'callback_data' => 'newList']، ['text' => '- Up To Old List.'، 'callback_data' => 'إلحاق']] و
						[['text' => '- رجوع.'، 'callback_data' => 'back']]،
						[['text' => '- 𝙳𝚎𝚟𝚎𝚕𝚘𝚙𝚎𝚛 𝚌𝚑𝚊𝚗𝚗𝚎𝚕 𝄋.'، 'url' => 'T.me/IIQQTQ']] ،
                    ]
                ])
            ]) ؛
          } elseif ($ data == 'Explore') {
            exec ('screen -dmS gr php Explore.php') ؛
          } elseif ($ data == 'status') {
					حالة $ = "؛
					foreach (حسابات $ كـ $ account => $ ac) {
						$ c = explode (':'، $ account) [0]؛
						$ x = exec ('screen -S'. $ c. '-Q select.؛ echo $؟')؛
						إذا ($ x == '0') {
				        حالة $. = "- $ account => العمل. \ n"؛
				    } آخر {
				        حالة $. = "- $ account => Sleep. \ n"؛
				    }
					}
					$ bot-> sendMessage ([
							'chat_id' => $ chatId ،
							'text' => "- فحص الحالة => \ n $ status."،
							'parse_mode' => 'تخفيض السعر'
						]) ؛
				} elseif ($ data == 'back') {
          	$ bot-> تحرير نص الرسالة ([
                      'chat_id' => $ chatId ،
                      'message_id' => متوسط ​​دولار ،
                   'text' => "- 𝐖𝐄𝐋𝐂𝐎𝐌𝐄 𝐓𝐎 𝐓𝐇𝐄 𝐅𝐈𝐒𝐇𝐈𝐍𝐆 𝐓𝐎𝐎𝐋 𝐀𝐂𝐂𝐎𝐔𝐍𝐓𝐒
𝐏𝐑𝐎𝐆𝐑𝐀𝐌𝐌𝐄𝐃 𝐁𝐘 @ E_5_O. "،
                  'reply_markup' => json_encode ([
                      "inline_keyboard" => [
                          [['text' => '- إضافة حساب.'، 'callback_data' => 'تسجيل الدخول']]،
                          [['text' => '- Grab Settings.'، 'callback_data' => 'grabber']] ،
                          [['text' => '- بدء الفحص.'، 'callback_data' => 'run']، ['text' => '- Stop Check.'، 'callback_data' => 'stop']]،
						  [['text' => '- حالة الأداة.'، 'callback_data' => 'status']]،
						  [['text' => '- 𝙳𝚎𝚟𝚎𝚕𝚘𝚙𝚎𝚛 𝚌𝚑𝚊𝚗𝚗𝚎𝚕 𝄋.'، 'url' => 'T.me/IIQQTQ']] ،
                      ]
                  ])
                  ]) ؛
          } آخر {
          	$ data = explode ('&'، $ data)؛
          	إذا ($ data [0] == 'del') {
          		
          		unset (حسابات $ [$ data [1]]) ؛
          		file_put_contents ('accounts.json'، json_encode (حسابات $)) ؛
              لوحة المفاتيح $ = ['inline_keyboard' => [
							[['text' => "- إضافة حساب جديد."، 'callback_data' => 'addL']]
									]] ؛
		              foreach (حسابات $ كـ $ account => $ v) {
		                  $ keyboard ['inline_keyboard'] [] = [['text' => $ account، 'callback_data' => 'ddd']، ['text' => "- LogOut"، 'callback_data' => 'del &'. حساب $]] ؛
		              }
		              $ keyboard ['inline_keyboard'] [] = [['text' => '- رجوع.'، 'callback_data' => 'back']]؛
		              $ bot-> editMessageText ([
		                  'chat_id' => $ chatId ،
		                  'message_id' => متوسط ​​دولار ،
		                  'text' => "- التحكم في الحسابات."،
		                  'reply_markup' => json_encode (لوحة المفاتيح $)
		              ]) ؛
          	} elseif ($ data [0] == 'Forg') {
          	  $ config ['for'] = $ data [1] ؛
          	  file_put_contents ('config.json'، json_encode ($ config)) ؛
              $ for = $ config ['for']! = فارغ؟ $ config ['for']: 'Select'؛
              $ count = count (file_get_contents ($ for)) ؛
              $ bot-> editMessageText ([
                'chat_id' => $ chatId ،
                'message_id' => متوسط ​​دولار ،
                'text' => "- قائمة المستخدمين. \ n- عدد المستخدمين => $ count. \ n- الحساب قيد الاستخدام => $ for."،
                'reply_markup' => json_encode ([
                    "inline_keyboard" => [
                        [['text' => '- من البحث.'، 'callback_data' => 'بحث']]،
                        [['text' => '- From Hashtag (#).'، 'callback_data' => 'hashtag']، ['text' => '- From Explore.'، 'callback_data' => 'Explore']] و
                        [['text' => '- From Followers.'، 'callback_data' => 'Followers']، ['text' => "- From Follow."، 'callback_data' => 'follow']]،
                        [['text' => "- الحساب قيد الاستخدام: $ مقابل."، 'callback_data' => 'for']]،
                        [['text' => '- إزالة كل المستخدمين.'، 'callback_data' => 'newList']، ['text' => '- Up To Old List.'، 'callback_data' => 'إلحاق']] و
						[['text' => '- رجوع.'، 'callback_data' => 'back']]،
						[['text' => '- 𝙳𝚎𝚟𝚎𝚕𝚘𝚙𝚎𝚛 𝚌𝚑𝚊𝚗𝚗𝚎𝚕 𝄋.'، 'url' => 'T.me/IIQQTQ']] ،
                    ]
                ])
            ]) ؛
          	} elseif ($ data [0] == 'start') {
          	  file_put_contents ('screen'، $ data [1])؛
          	  $ bot-> تحرير نص الرسالة ([
                      'chat_id' => $ chatId ،
                      'message_id' => متوسط ​​دولار ،
                      'text' => "- 𝐖𝐄𝐋𝐂𝐎𝐌𝐄 𝐓𝐎 𝐓𝐇𝐄 𝐅𝐈𝐒𝐇𝐈𝐍𝐆 𝐓𝐎𝐎𝐋 𝐀𝐂𝐂𝐎𝐔𝐍𝐓𝐒
𝐏𝐑𝐎𝐆𝐑𝐀𝐌𝐌𝐄𝐃 𝐁𝐘 @ E_5_O. "،
                  'reply_markup' => json_encode ([
                      "inline_keyboard" => [
                          [['text' => '- إضافة حساب.'، 'callback_data' => 'تسجيل الدخول']]،
                          [['text' => '- Grab Settings.'، 'callback_data' => 'grabber']] ،
                          [['text' => '- بدء الفحص.'، 'callback_data' => 'run']، ['text' => '- Stop Check.'، 'callback_data' => 'stop']]،
						  [['text' => '- حالة الأداة.'، 'callback_data' => 'status']]،
						  [['text' => '- 𝙳𝚎𝚟𝚎𝚕𝚘𝚙𝚎𝚛 𝚌𝚑𝚊𝚗𝚗𝚎𝚕 𝄋.'، 'url' => 'T.me/IIQQTQ']] ،
                      ]
                  ])
                  ]) ؛
              exec ('screen -dmS' .explode (':'، $ data [1]) [0]. 'php start.php')؛
              $ bot-> sendMessage ([
                'chat_id' => $ chatId ،
                'text' => "- بدء الفحص. \ n- الحساب:" .explode (':'، $ data [1]) [0]. ' . '،
                'parse_mode' => 'تخفيض السعر'
              ]) ؛
          	} elseif ($ data [0] == 'stop') {
          	  $ bot-> تحرير نص الرسالة ([
                      'chat_id' => $ chatId ،
                      'message_id' => متوسط ​​دولار ،
                      'text' => "- 𝐖𝐄𝐋𝐂𝐎𝐌𝐄 𝐓𝐎 𝐓𝐇𝐄 𝐅𝐈𝐒𝐇𝐈𝐍𝐆 𝐓𝐎𝐎𝐋 𝐀𝐂𝐂𝐎𝐔𝐍𝐓𝐒
𝐏𝐑𝐎𝐆𝐑𝐀𝐌𝐌𝐄𝐃 𝐁𝐘 @ E_5_O. "،
                  'reply_markup' => json_encode ([
                      "inline_keyboard" => [
                          [['text' => '- إضافة حساب.'، 'callback_data' => 'تسجيل الدخول']]،
                          [['text' => '- Grab Settings.'، 'callback_data' => 'grabber']] ،
                          [['text' => '- بدء الفحص.'، 'callback_data' => 'run']، ['text' => '- Stop Check.'، 'callback_data' => 'stop']]،
						  [['text' => '- حالة الأداة.'، 'callback_data' => 'status']]،
						  [['text' => '- 𝙳𝚎𝚟𝚎𝚕𝚘𝚙𝚎𝚛 𝚌𝚑𝚊𝚗𝚗𝚎𝚕 𝄋.'، 'url' => 'T.me/IIQQTQ']] ،
                      ]
                    ])
                  ]) ؛
              exec ('screen -S' .explode (':'، $ data [1]) [0]. '-X quit')؛
          	}
          }
			}
		}
	} ؛
	$ bot = EzTG جديد (مصفوفة ('throw_telegram_errors' => false، 'token' => $ token، 'callback' => $ callback)) ؛
} catch (استثناء $ e) {
	صدى $ e-> getMessage (). PHP_EOL ؛
	ينام (1) ؛
}
