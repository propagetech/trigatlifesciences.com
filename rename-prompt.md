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
      "title": "TRIGAT LIFE SCIENCES | OUR COMPANY",
      "first_heading": "OUR COMPANY"
    }
  },
  {
    "path": "careers.html",
    "context": {
      "title": "TRIGAT LIFE SCIENCES | CAREERS",
      "first_heading": "CAREERS"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "TRIGAT LIFE SCIENCES | CONTACT US",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
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
    "path": "css/abf7b1c9643a77b46ff8e5b5443fb5eb.css",
    "context": {
      "path": "css/abf7b1c9643a77b46ff8e5b5443fb5eb.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/daf317778aab94d537d8f8b317f3b05c.css",
    "context": {
      "path": "css/daf317778aab94d537d8f8b317f3b05c.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "directors.html",
    "context": {
      "title": "TRIGAT LIFE SCIENCES | DIRECTORS",
      "first_heading": "DIRECTORS"
    }
  },
  {
    "path": "imgs/07787b14ec58a67283bd998b8ebd077c.webp",
    "context": {
      "refs": [
        {
          "alt": "BROBIO Syrup",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e0277ff6c84bdbd67c8e25e9b348680.webp",
    "context": {
      "refs": [
        {
          "alt": "NOTIAN 100 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ef0b8dd60500f92b665ac106ba372ac.webp",
    "context": {
      "refs": [
        {
          "alt": "LITHOJET 450 SR Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/10cb021f3ee6bbb1cc9c33262820d357.webp",
    "context": {
      "refs": [
        {
          "alt": "HI \u2013 GLOW Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/14787d1f9f8b5485ccab1ef90268167d.webp",
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
    "path": "imgs/14da1b7bc61e33b00803fc6dcd8d9986.webp",
    "context": {
      "refs": [
        {
          "alt": "ORTHOGAT Oil",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/18e928bf727a31491808ebbc6a090532.webp",
    "context": {
      "refs": [
        {
          "alt": "FLITRA - 100/200 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1fa1fe2b3e38bf0803a358b22c5dd6a3.webp",
    "context": {
      "refs": [
        {
          "alt": "KLOJET \u2013 ES Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/27451a70f097c8231dac279d643f09d6.webp",
    "context": {
      "refs": [
        {
          "alt": "PRAXY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2764f8e3714be25664a318cb79ed6857.webp",
    "context": {
      "refs": [
        {
          "alt": "PETRA 40 Tablets",
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
    "path": "imgs/2cda46cc0a5cf1bbb9fdf1c4d7d0cba6.webp",
    "context": {
      "refs": [
        {
          "alt": "APIHEP Syrup",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2fbe7504f33c9c87f90806d00f88de1c.webp",
    "context": {
      "refs": [
        {
          "alt": "BUSTIN",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3038d4806c85d95915f6ed3b9eda3342.webp",
    "context": {
      "refs": [
        {
          "alt": "RIBOTAG \u2013 DSR Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3128f9f127ec525d232000372f350ac7.webp",
    "context": {
      "refs": [
        {
          "alt": "COB 5/10 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3619667f3166ea4b5ede84c39fc6951b.webp",
    "context": {
      "refs": [
        {
          "alt": "VOCE \u2013 LV Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3667f43790e54017af3f2d77bf7a48f3.webp",
    "context": {
      "refs": [
        {
          "alt": "LAR\u2013CZ Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/37f219d375765d1f86fed041eec41a09.webp",
    "context": {
      "refs": [
        {
          "alt": "TOCID Gel",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b1fc0e46f06de4a854db8b6def13c35.webp",
    "context": {
      "refs": [
        {
          "alt": "VOCE- M Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3f87c3edb6cf340bef7f0139ae873837.webp",
    "context": {
      "refs": [
        {
          "alt": "REMO \u2013 MD Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/45ccee9552b7d4610008375eaacc08cb.webp",
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
    "path": "imgs/47919b529cf01962d8d3ec2a5f4d049c.webp",
    "context": {
      "refs": [
        {
          "alt": "CIFITRAP 200 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/48efaa26dfba3b4d4c46a7dea578c25c.webp",
    "context": {
      "refs": [
        {
          "alt": "AMITIG 10/25 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4aa2b6e508ec3b8d3ea9059191276242.webp",
    "context": {
      "refs": [
        {
          "alt": "AMITIG PLUS/FORTE Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4abd81e41e27b93862397f0af04860c4.webp",
    "context": {
      "refs": [
        {
          "alt": "PREL- AM Cough Syrup",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4bda28105978bcfc07dde1605359025d.webp",
    "context": {
      "refs": [
        {
          "alt": "ZOLOJET Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/56c2b6a16e61ac43018131eed1b08a83.webp",
    "context": {
      "refs": [
        {
          "alt": "TROZ \u2013 S- 1500 inj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5917e5f975fdc092017c63f1ccbf9159.webp",
    "context": {
      "refs": [
        {
          "alt": "ONDOGAT inj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5a1bf0976a8284f2ac3779bd627eea94.webp",
    "context": {
      "refs": [
        {
          "alt": "About Us",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5bc508e76fb42087640ecc7378581005.webp",
    "context": {
      "refs": [
        {
          "alt": "CILONIC Gel",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ecc85b2d3f96c83f78267b6c0d470b7.webp",
    "context": {
      "refs": [
        {
          "alt": "KLOJET \u2013 MD Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/628dc8b138e255720a9c8deb3e742632.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6686d208fd5012f628bfd25200048ba9.webp",
    "context": {
      "refs": [
        {
          "alt": "ZITRA 5/10 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67f24256a89f569cd5431137051a234c.webp",
    "context": {
      "refs": [
        {
          "alt": "ARTEEFA inj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6a1ba7c95f49a7ad8ad4bcd1356cb39d.webp",
    "context": {
      "refs": [
        {
          "alt": "TRUX Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6c35bfb3c52c2de41e740ce3335007c9.webp",
    "context": {
      "refs": [
        {
          "alt": "NEUROGAT capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d30ea49fc8a892f513f62637ee0567b.webp",
    "context": {
      "refs": [
        {
          "alt": "TROZEN \u2013 P Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6f028fab0453eb4fb581cbd924b52cc9.webp",
    "context": {
      "refs": [
        {
          "alt": "TRIFT 2/5 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6fd95ac19f074a00eb865b4f0107ce7f.webp",
    "context": {
      "refs": [
        {
          "alt": "CILONIC SR Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7a5536f8c3f68b297db6f80fabf0acc3.webp",
    "context": {
      "refs": [
        {
          "alt": "FLUSEE 20/40/60 Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7dbeb66f322d43c6f822941933a4621f.webp",
    "context": {
      "refs": [
        {
          "alt": "CIFITRAP \u2013O Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8166b6f642e72cbdc0f008f14729ded0.webp",
    "context": {
      "refs": [
        {
          "alt": "CITOJET Tablets/Inj",
          "title": ""
        },
        {
          "alt": "CITOJET ing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/82b54d3878ce4c2710aa6edef91d6768.webp",
    "context": {
      "refs": [
        {
          "alt": "PYRA 650mg",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8733ec78c6ce73c7faa0d5f73da417a5.webp",
    "context": {
      "refs": [
        {
          "alt": "NANDOK- 25/50 inj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/884c11cfa055973d5999d1e083b4758c.webp",
    "context": {
      "refs": [
        {
          "alt": "TEEALFA inj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8ba6b1481a93b58dcd953ee0bb3953b1.webp",
    "context": {
      "refs": [
        {
          "alt": "RECTOF\u2013OZ Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f1d08f9397c7dfdea5b11366abe8243.webp",
    "context": {
      "refs": [
        {
          "alt": "TROZEN inj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/930b626419ca9af868ac23e51e47a151.webp",
    "context": {
      "refs": [
        {
          "alt": "MOZAM 0.25/0.50 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/983f54ff8b0b289cabc930bb992b5754.webp",
    "context": {
      "refs": [
        {
          "alt": "BLEN 5/10/25 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9873f8ff1a5a6f6075087b21a0e44f28.webp",
    "context": {
      "refs": [
        {
          "alt": "ATROJET \u2013 AM Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/99e7508c227f636703100b3a6a22875e.webp",
    "context": {
      "refs": [
        {
          "alt": "FLUNIF 5/10 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e76cdd99069a83164d4cde6f739dcf4.webp",
    "context": {
      "refs": [
        {
          "alt": "PRAGIL- M Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e7fc9f0204caf45386bd6ccf75f52dd.webp",
    "context": {
      "refs": [
        {
          "alt": "CALCIAT Sachets/Soft Gel Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9f21b0532023c4051250a41ef215b72a.webp",
    "context": {
      "refs": [
        {
          "alt": "ZYNIM \u2013 P Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0370ddd2dad20a71fc2de7b575a6989.webp",
    "context": {
      "refs": [
        {
          "alt": "CRUSTER Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a53f0c39ca836f1a372a0e234afa1d8c.webp",
    "context": {
      "refs": [
        {
          "alt": "OXEZER 150/300 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a5f89d7fca9e1e07dea1cbcf304634d1.webp",
    "context": {
      "refs": [
        {
          "alt": "NEUROGAT inj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a949499da5f0219a92c210e4de8c7c53.webp",
    "context": {
      "refs": [
        {
          "alt": "SOVALIC CR 200/300/500 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a992d246c49150f4714786f09697dddc.webp",
    "context": {
      "refs": [
        {
          "alt": "TRUX Syrup",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aa59844f9b016ba2cc7261f3c82d8baf.webp",
    "context": {
      "refs": [
        {
          "alt": "LAXLIPO Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ab06dc1f54d89959a50941499f007347.webp",
    "context": {
      "refs": [
        {
          "alt": "PETRA inj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ab27b38a2e61bb223e80d8dd7300dd87.webp",
    "context": {
      "refs": [
        {
          "alt": "FLUTAG 150 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/acc4d861570d24ab42b371f2b487c5b3.webp",
    "context": {
      "refs": [
        {
          "alt": "ZICOTROL Soft Gel Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/adec787a0f25bf42a3bdf1137203d788.webp",
    "context": {
      "refs": [
        {
          "alt": "Manufacturing Unit",
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
    "path": "imgs/b167b4c0b571de9572182c8a06651e9a.webp",
    "context": {
      "refs": [
        {
          "alt": "CILONIC \u2013 P Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b2e06805cf6d1f73c9b44405163851bb.webp",
    "context": {
      "refs": [
        {
          "alt": "TROPIT 25/50 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5987ab69dc7a453e485f468c851fa65.webp",
    "context": {
      "refs": [
        {
          "alt": "ESITOPA 10/20 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b792dd813cb268b8f4682c2ba0e575b7.webp",
    "context": {
      "refs": [
        {
          "alt": "TRIOLIV Syrup/Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b795ed29dcb50442b9a0734ed88fe97c.webp",
    "context": {
      "refs": [
        {
          "alt": "RELISER Syrup",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b8aac4939716febb5b3ddf64d299bc74.webp",
    "context": {
      "refs": [
        {
          "alt": "KEEDU\u2013IR Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9a8030753d162a43f375cddf4199ae3.webp",
    "context": {
      "refs": [
        {
          "alt": "SULEP 100/200/400 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bb6dd2010ddaa18ddb09bde2054e0702.webp",
    "context": {
      "refs": [
        {
          "alt": "PZOBA inj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bd068bbd5b8166f30616e03a6ab59702.webp",
    "context": {
      "refs": [
        {
          "alt": "OLATIG 5/10/15 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf486153387e21ddb4939a804d6a9aad.webp",
    "context": {
      "refs": [
        {
          "alt": "LEVATE Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c266857d252eb32d32a3b882d5597f38.webp",
    "context": {
      "refs": [
        {
          "alt": "ACEKEM- MR Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c2cf3c3d1dea5847086ff4cada77907d.webp",
    "context": {
      "refs": [
        {
          "alt": "SHEKALP Syrup",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c595d13fb4d5a70446a01ffb6de2220e.webp",
    "context": {
      "refs": [
        {
          "alt": "PIRAJET Tablets/Syrup",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c720b43a05989f80c24ab6c2ec8e7f6e.webp",
    "context": {
      "refs": [
        {
          "alt": "LORATIG 1 / 2 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c754b688cd115ca1480c1f77ad4a52e2.webp",
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
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d1184b6668360c225ef61e6946425297.webp",
    "context": {
      "refs": [
        {
          "alt": "DANFU 20/30/40/60 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d1445baa5a922cfca2de2fa31636bc1b.webp",
    "context": {
      "refs": [
        {
          "alt": "RECTOF 200 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d8689b54166cd092d41434daec28546f.webp",
    "context": {
      "refs": [
        {
          "alt": "TRIFT PLUS Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d90c45712f45e0cdd1c35d768ee19f5e.webp",
    "context": {
      "refs": [
        {
          "alt": "PETRA \u2013 D/ DS Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db05763735c3ba51254db80d79b51d56.webp",
    "context": {
      "refs": [
        {
          "alt": "LEVATE Inj",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dd91a4746cdb61d3511116acc6e9e030.webp",
    "context": {
      "refs": [
        {
          "alt": "CAROBEX Soft Gel Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e2878475b878683b3306181fa755df16.webp",
    "context": {
      "refs": [
        {
          "alt": "DIGEM Syrup",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e8283585de07b6fab50602a3a2386151.webp",
    "context": {
      "refs": [
        {
          "alt": "VOCE- M Kid",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eab3fa29a878f014f23abc7cbc825dfd.webp",
    "context": {
      "refs": [
        {
          "alt": "MOZAM ES Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb274e178b217079336ef1119ccb8947.webp",
    "context": {
      "refs": [
        {
          "alt": "DIFNOX 120/180 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec021fc456eba0608e2a9f4876c5be1e.webp",
    "context": {
      "refs": [
        {
          "alt": "AT-PRO Powder",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec72640751f1c15a64eac6ebafe7881a.webp",
    "context": {
      "refs": [
        {
          "alt": "GIBINOR Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ed222144d26db7d5966289cbfca373b1.webp",
    "context": {
      "refs": [
        {
          "alt": "Philosophy",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eda43f4b5e0d1a8270fab61edacbd923.webp",
    "context": {
      "refs": [
        {
          "alt": "CALUM Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ee981e6b2f0a89922d990c065fd4b1c7.webp",
    "context": {
      "refs": [
        {
          "alt": "POPILAN TR 40 Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef397c2ba4ad3ddebfb0bc8dadd7361a.webp",
    "context": {
      "refs": [
        {
          "alt": "SERTIG 50/100 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0328b792baea4fd3609103715c6fd47.webp",
    "context": {
      "refs": [
        {
          "alt": "RESPORA 3/PLUS 3 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f4a5f900aba776a727d653aea1f26ed9.webp",
    "context": {
      "refs": [
        {
          "alt": "POPILAN 10/20 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f6a017abc7c5509a2bf7f2bf81daf298.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f78d686e139d6f4f0b2ec9f356827747.webp",
    "context": {
      "refs": [
        {
          "alt": "PEXERT CR Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f85bc20532e8f73d95666a0bf54f33a1.webp",
    "context": {
      "refs": [
        {
          "alt": "PRAGIL 75 Capsules",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fb1ad75c8765584c0fc5965ac6f2eba0.webp",
    "context": {
      "refs": [
        {
          "alt": "TIDEP 10/20 Tablets",
          "title": ""
        },
        {
          "alt": "TIDEP 10/20 Tablets",
          "title": ""
        },
        {
          "alt": "TIDEP 10/20 Tablets",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fb1dc6e3829cb7e22cb60a0eeccebf41.webp",
    "context": {
      "refs": [
        {
          "alt": "PREL \u2013 DM Plus Cough Syrup",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "TRIGAT LIFE SCIENCES | HOME",
      "first_heading": "\u0938\u0930\u094d\u0935\u0947 \u092d\u0935\u0928\u094d\u0924\u0941 \u0938\u0941\u0916\u093f\u0928: \u0938\u0930\u094d\u0935\u0947 \u0938\u0928\u094d\u0924\u0941 \u0928\u093f\u0930\u093e\u092e\u092f\u093e:"
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
    "path": "js/5133aee136471c84556b248a1089b385.js",
    "context": {
      "path": "js/5133aee136471c84556b248a1089b385.js"
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
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "mystic.html",
    "context": {
      "title": "TRIGAT LIFE SCIENCES | MYSTIC",
      "first_heading": "MYSTIC"
    }
  },
  {
    "path": "products.html",
    "context": {
      "title": "TRIGAT LIFE SCIENCES | PRODUCTS",
      "first_heading": "PRODUCTS"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.