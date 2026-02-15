You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "AEROHELICON & AVIATION | ABOUT US",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "associates-partners.html",
    "context": {
      "title": "AEROHELICON & AVIATION | ASSOCIATES & PARTNERS",
      "first_heading": "ASSOCIATES & PARTNERS"
    }
  },
  {
    "path": "career.html",
    "context": {
      "title": "AEROHELICON & AVIATION | CAREER",
      "first_heading": "CAREER"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "AEROHELICON & AVIATION | CONTACT US",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/595cb6ccb56826a802ed411cef875f0e.css",
    "context": {
      "path": "css/595cb6ccb56826a802ed411cef875f0e.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/e980cb6b50645ddc9d24377f2fe05d53.css",
    "context": {
      "path": "css/e980cb6b50645ddc9d24377f2fe05d53.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "draft.html",
    "context": {
      "title": "AEROHELICON & AVIATION | HOME",
      "first_heading": "Put in the title of your section here."
    }
  },
  {
    "path": "imgs/0d59a15fb7ca410b301ace703dd2b4c7.webp",
    "context": {
      "refs": [
        {
          "alt": "AEROHELICON & AVIATION PVT LTD",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e791c43ded02d25884fb13c3c11bb7d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "TRAINING & DEVELOPMENT",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1170aaa4477810ffc4e3fa7375b7623f.webp",
    "context": {
      "refs": [
        {
          "alt": "MISSION & OBJECTIVES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1731033df1cd8da1a8d3ec6b0d3b8705.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM11",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1943f39760860984b6b71f8d04ca0f03.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11019PM7",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1c3c983b26c7ff92c9426c2b70a8e7fe.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11348PM1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/242401e9f29b00c0b834fd2c7dd6a4ef.webp",
    "context": {
      "refs": [
        {
          "alt": "81013658m",
          "title": ""
        },
        {
          "alt": "ENGINEERING SERVICES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2f607c40bbfea20cfb6c9f25f59bffa5.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11020PM1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/443c6e74392e74c59f6d30a9997a7129.webp",
    "context": {
      "refs": [
        {
          "alt": "CHARTER FLIGHTS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46d1ffffa65e91e81cc9eeeadadcf03e.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11020PM3",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/49241af95d51d0c491672d7259662c38.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM15",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4d172187291d0d9735f7de18cc6ada6c.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11020PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/575da868c3836458ab4f3bfe80f90718.webp",
    "context": {
      "refs": [
        {
          "alt": "Title goes here!",
          "title": ""
        },
        {
          "alt": "Title goes here!",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5a8a6400edfbcb14f4ed4718deb4fa47.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM13",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e1d076d77f536641bdaac7bf4ec3490.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM7",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5f930c12345a5e58498f5bb12b82e8f2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62c256ea16df092cc60b0f1c100d0bac.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/650c985e947689ee1170950b4d48c156.webp",
    "context": {
      "refs": [
        {
          "alt": "WHY US",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/679cc906b7afde1f1397d631112fca7d.webp",
    "context": {
      "refs": [
        {
          "alt": "Mr. S.Madhu Sudan",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/684036dd5fbf2c6c707ec487eb17b1d9.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11018PM3",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70361f9843b078a5b008542bea854b03.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11348PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/74ac5689b83d242989083f9c5b91dece.webp",
    "context": {
      "refs": [
        {
          "alt": "Coming Soon",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/750bc35b683f3af70f0f4ff0bc1a911c.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11019PM4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7822ac19d42198584f0288d642cee8bd.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11019PM6",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78de2e6e75b5102fa3dd5a8486557b8d.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11018PM1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7a487fa81c4edca0629ce4f2b9b027f4.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at10901PM3",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ecb13f827f759b35b04b8e4d475ef32.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/866f582f0d506ae35c207f2994a677be.webp",
    "context": {
      "refs": [
        {
          "alt": "Wheels and Brakes",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8fd8213218a93e6d2535eb6106e62d44.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM14",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9330bfddafd8af34bd307746187c72f0.webp",
    "context": {
      "refs": [
        {
          "alt": "MANUFACTURING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9500cfe3b0efc207cfd74ee01f314ce9.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "Helicon Aerospace & Aviation Pvt Ltd was started in 2017 at Bangalore, India by aerospace experts wi",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/95678dcc39231ab539c9d4e8deb339ec.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "MRO",
          "title": ""
        },
        {
          "alt": "Title for this section goes here!",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/96145c5a469b190a5ea6586e2f6d90f6.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11021PM1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/988a2cd4dfa494b01dc238f24e0d7a27.webp",
    "context": {
      "refs": [
        {
          "alt": "LM",
          "title": ""
        },
        {
          "alt": "LINE MAINTENANCE",
          "title": ""
        },
        {
          "alt": "Line Maintenance",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/994418cd701c4a11c9a3bfadede7d637.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at10901PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9df5402b1b515ae3f6dd3271d8b98654.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0abe2f45476e467831e5b665ab3b5a7.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM17",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ab1c56919b458f1f3f68a077ec2f2b1a.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM18",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad762bc7e788167299dd843c57c2adf8.webp",
    "context": {
      "refs": [
        {
          "alt": "NDT (Non-Destructive Testing)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b06adefcc4baa0e240f3d02d462d0b7e.webp",
    "context": {
      "refs": [
        {
          "alt": "Mr. ASHOK KUMAR SAXENA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ba4980193e0e7f209ba8bcae0a6b57e7.webp",
    "context": {
      "refs": [
        {
          "alt": "OTHER SERVICES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bcd8be559af250ef12eb449adaa85d9d.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM6",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c04efeb27958a043b97e96d020d89b45.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11020PM4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cb50fe6cc0c89227ac6c6efd6ff84748.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM16",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cc25d0b60c3e1ad7de4c8f6f28dd1895.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11019PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0404599a53eeb1df52e3b46671b7d2d.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11018PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d250e1e475ae0e4b40ed7e2c1daeb39a.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at10902PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e589c32fe02eec0730eb9e631cbac19d.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM8",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e9b7c4208d4f8f116bdc5d156721d1f7.webp",
    "context": {
      "refs": [
        {
          "alt": "WHEELS AND BRAKES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec719479ba892462654876ef8b53afe0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "VISION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eee62ea64d2955743fdfa56d7308d06d.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f2b7866457221c4d3cb3419abd270222.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at10901PM1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f6e2c6770f79e84a5f3c201365c52d74.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20230924at11349PM10",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "AEROHELICON & AVIATION | HOME",
      "first_heading": "AEROHELICON PVT LTD"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/21fe4170138ba83cdef48aad487a0909.js",
    "context": {
      "path": "js/21fe4170138ba83cdef48aad487a0909.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "news-media.html",
    "context": {
      "title": "AEROHELICON & AVIATION | NEWS & MEDIA",
      "first_heading": "NEWS & MEDIA"
    }
  },
  {
    "path": "services.html",
    "context": {
      "title": "AEROHELICON & AVIATION | SERVICES",
      "first_heading": "SERVICES"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.