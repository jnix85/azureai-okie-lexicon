# Oklahoma Regional Dialect Custom Lexicon for Azure AI Speech

This document provides a production-ready **Pronunciation Lexicon Specification (PLS) Version 1.0** XML file for Azure AI Speech Services (Text-to-Speech), specifically tuned for the **Oklahoma regional dialect** (a transitional blend of South Midland, Southern, Western American English, and Indigenous tribal toponyms).

---

## 1. Quick Start: SSML Integration

To use this custom lexicon in Azure AI Speech:
1. Save the XML block below as `oklahoma_lexicon.pls` (or `oklahoma_lexicon.xml`).
2. Upload the file to an HTTPS endpoint (e.g., Azure Blob Storage with anonymous public read access or a Shared Access Signature URI).
3. Reference it in your SSML using the `<lexicon>` tag inside `<voice>`.

```xml
<speak version="1.0" xmlns="http://www.w3.org/2001/10/synthesis"
       xmlns:mstts="http://www.w3.org/2001/mstts"
       xml:lang="en-US">
    <voice name="en-US-AvaNeural">
        <!-- Replace URI with your Azure Blob Storage SAS URL or public HTTPS link -->
        <lexicon uri="https://mystorageaccount.blob.core.windows.net/lexicons/oklahoma_lexicon.pls"/>
        
        Welcome to Oklahoma! Yesterday we drove from Prague through Chickasha and Tahlequah, 
        stopped near Miami for some pecan pie, and then grabbed an onion burger down near Gotebo. 
        Don't forget to check your car insurance before you head over yonder!
    </voice>
</speak>
```

---

## 2. Custom Lexicon File: `oklahoma_lexicon.pls`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<lexicon version="1.0" 
         xmlns="http://www.w3.org/2005/01/pronunciation-lexicon"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://www.w3.org/2005/01/pronunciation-lexicon 
                             http://www.w3.org/TR/2007/CR-pronunciation-lexicon-20071212/pls.xsd"
         alphabet="ipa" 
         xml:lang="en-US">

  <!-- ================================================================= -->
  <!-- 1. OKLAHOMA TOPONYMS & PLACES (Frequently Mispronounced by TTS)   -->
  <!-- ================================================================= -->

  <!-- Prague: Locally pronounced "PRAYG" (rhymes with plague/vague, not Czech capital) -->
  <lexeme>
    <grapheme>Prague</grapheme>
    <grapheme>prague</grapheme>
    <phoneme>ˈpɹeɪg</phoneme>
  </lexeme>

  <!-- Miami: Locally pronounced "my-AM-uh" (never "my-AM-ee" like Florida) -->
  <lexeme>
    <grapheme>Miami</grapheme>
    <grapheme>miami</grapheme>
    <phoneme>maɪ.ˈæ.mə</phoneme>
  </lexeme>

  <!-- Chickasha: Locally pronounced "CHICK-uh-shay" (not "Chick-a-shaw") -->
  <lexeme>
    <grapheme>Chickasha</grapheme>
    <grapheme>chickasha</grapheme>
    <phoneme>ˈtʃɪk.ə.ʃeɪ</phoneme>
  </lexeme>

  <!-- Gotebo: Locally pronounced "GO-tee-boh" (Kiowa origin) -->
  <lexeme>
    <grapheme>Gotebo</grapheme>
    <grapheme>gotebo</grapheme>
    <phoneme>ˈgoʊ.ti.boʊ</phoneme>
  </lexeme>

  <!-- Nowata: Locally pronounced "no-WAY-tuh" (Delaware/Lenape origin nuwita) -->
  <lexeme>
    <grapheme>Nowata</grapheme>
    <grapheme>nowata</grapheme>
    <phoneme>noʊ.ˈweɪ.tə</phoneme>
  </lexeme>

  <!-- Okmulgee: Locally pronounced "oke-MUL-ghee" (Muscogee Creek origin) -->
  <lexeme>
    <grapheme>Okmulgee</grapheme>
    <grapheme>okmulgee</grapheme>
    <phoneme>oʊk.ˈmʌl.gi</phoneme>
  </lexeme>

  <!-- Tahlequah: Capital of the Cherokee Nation ("TAL-uh-kwah") -->
  <lexeme>
    <grapheme>Tahlequah</grapheme>
    <grapheme>tahlequah</grapheme>
    <phoneme>ˈtæ.lə.kwɑ</phoneme>
  </lexeme>

  <!-- Eufaula: Locally pronounced "yoo-FAW-luh" -->
  <lexeme>
    <grapheme>Eufaula</grapheme>
    <grapheme>eufaula</grapheme>
    <phoneme>ju.ˈfɔ.lə</phoneme>
  </lexeme>

  <!-- Muskogee: "muss-KOH-ghee" -->
  <lexeme>
    <grapheme>Muskogee</grapheme>
    <grapheme>muskogee</grapheme>
    <phoneme>mʌs.ˈkoʊ.gi</phoneme>
  </lexeme>

  <!-- Ouachita: Locally pronounced "WASH-ih-tah" -->
  <lexeme>
    <grapheme>Ouachita</grapheme>
    <grapheme>ouachita</grapheme>
    <phoneme>ˈwɑ.ʃɪ.tɑ</phoneme>
  </lexeme>

  <!-- Talihina: "tal-uh-HEE-nuh" (Choctaw origin) -->
  <lexeme>
    <grapheme>Talihina</grapheme>
    <grapheme>talihina</grapheme>
    <phoneme>ˌtæ.lə.ˈhi.nə</phoneme>
  </lexeme>

  <!-- Tishomingo: Capital of the Chickasaw Nation ("tish-uh-MING-goh") -->
  <lexeme>
    <grapheme>Tishomingo</grapheme>
    <grapheme>tishomingo</grapheme>
    <phoneme>ˌtɪʃ.ə.ˈmɪŋ.goʊ</phoneme>
  </lexeme>

  <!-- Sapulpa: "suh-PULL-puh" (Creek chief Sapulpa) -->
  <lexeme>
    <grapheme>Sapulpa</grapheme>
    <grapheme>sapulpa</grapheme>
    <phoneme>sə.ˈpʌl.pə</phoneme>
  </lexeme>

  <!-- Poteau: "POH-toh" -->
  <lexeme>
    <grapheme>Poteau</grapheme>
    <grapheme>poteau</grapheme>
    <phoneme>ˈpoʊ.toʊ</phoneme>
  </lexeme>

  <!-- Catoosa: "kuh-TOO-suh" (Cherokee origin) -->
  <lexeme>
    <grapheme>Catoosa</grapheme>
    <grapheme>catoosa</grapheme>
    <phoneme>kə.ˈtu.sə</phoneme>
  </lexeme>

  <!-- Coweta: Locally pronounced "cow-EE-tuh" (never "cow-etta") -->
  <lexeme>
    <grapheme>Coweta</grapheme>
    <grapheme>coweta</grapheme>
    <phoneme>kaʊ.ˈi.tə</phoneme>
  </lexeme>

  <!-- Atoka: "uh-TOE-kuh" (Choctaw chief Atoka) -->
  <lexeme>
    <grapheme>Atoka</grapheme>
    <grapheme>atoka</grapheme>
    <phoneme>ə.ˈtoʊ.kə</phoneme>
  </lexeme>

  <!-- Skiatook: "SKY-uh-took" (Cherokee origin) -->
  <lexeme>
    <grapheme>Skiatook</grapheme>
    <grapheme>skiatook</grapheme>
    <phoneme>ˈskaɪ.ə.tʊk</phoneme>
  </lexeme>

  <!-- Inola: Locally pronounced "eye-NO-luh" (Cherokee word for black fox) -->
  <lexeme>
    <grapheme>Inola</grapheme>
    <grapheme>inola</grapheme>
    <phoneme>aɪ.ˈnoʊ.lə</phoneme>
  </lexeme>

  <!-- Okemah: "oh-KEE-muh" (Kickapoo origin) -->
  <lexeme>
    <grapheme>Okemah</grapheme>
    <grapheme>okemah</grapheme>
    <phoneme>oʊ.ˈki.mə</phoneme>
  </lexeme>

  <!-- Wewoka: "wuh-WOH-kuh" (Seminole origin "barking water") -->
  <lexeme>
    <grapheme>Wewoka</grapheme>
    <grapheme>wewoka</grapheme>
    <phoneme>wə.ˈwoʊ.kə</phoneme>
  </lexeme>

  <!-- Pushmataha: "push-muh-tuh-HAH" -->
  <lexeme>
    <grapheme>Pushmataha</grapheme>
    <grapheme>pushmataha</grapheme>
    <phoneme>ˌpʊʃ.mə.tə.ˈhɑ</phoneme>
  </lexeme>

  <!-- Bokchito: "bohk-CHEE-toh" (Choctaw for big creek) -->
  <lexeme>
    <grapheme>Bokchito</grapheme>
    <grapheme>bokchito</grapheme>
    <phoneme>boʊk.ˈtʃi.toʊ</phoneme>
  </lexeme>

  <!-- Achille: Locally pronounced "uh-CHILL-ee" (not Achilles) -->
  <lexeme>
    <grapheme>Achille</grapheme>
    <grapheme>achille</grapheme>
    <phoneme>ə.ˈtʃɪl.i</phoneme>
  </lexeme>

  <!-- Chouteau: "SHOH-toh" -->
  <lexeme>
    <grapheme>Chouteau</grapheme>
    <grapheme>chouteau</grapheme>
    <phoneme>ˈʃoʊ.toʊ</phoneme>
  </lexeme>

  <!-- Cache: Locally pronounced "CASH" -->
  <lexeme>
    <grapheme>Cache</grapheme>
    <grapheme>cache</grapheme>
    <phoneme>ˈkæʃ</phoneme>
  </lexeme>

  <!-- Tonkawa: "TAHNG-kuh-wah" -->
  <lexeme>
    <grapheme>Tonkawa</grapheme>
    <grapheme>tonkawa</grapheme>
    <phoneme>ˈtɑŋ.kə.wɑ</phoneme>
  </lexeme>

  <!-- Pawhuska: Capital of Osage Nation ("paw-HUSS-kuh") -->
  <lexeme>
    <grapheme>Pawhuska</grapheme>
    <grapheme>pawhuska</grapheme>
    <phoneme>pɔ.ˈhʌs.kə</phoneme>
  </lexeme>

  <!-- Anadarko: "an-uh-DAR-koh" -->
  <lexeme>
    <grapheme>Anadarko</grapheme>
    <grapheme>anadarko</grapheme>
    <phoneme>ˌæ.nə.ˈdɑɹ.koʊ</phoneme>
  </lexeme>

  <!-- Cimarron: "SIM-uh-rahn" -->
  <lexeme>
    <grapheme>Cimarron</grapheme>
    <grapheme>cimarron</grapheme>
    <phoneme>ˈsɪm.ə.ɹɑn</phoneme>
  </lexeme>

  <!-- Kiamichi: Locally pronounced "kye-uh-MEE-shee" -->
  <lexeme>
    <grapheme>Kiamichi</grapheme>
    <grapheme>kiamichi</grapheme>
    <phoneme>ˌkaɪ.ə.ˈmi.ʃi</phoneme>
  </lexeme>

  <!-- Quapaw: "KWAH-paw" -->
  <lexeme>
    <grapheme>Quapaw</grapheme>
    <grapheme>quapaw</grapheme>
    <phoneme>ˈkwɑ.pɔ</phoneme>
  </lexeme>

  <!-- Wagoner: "WAG-ner" -->
  <lexeme>
    <grapheme>Wagoner</grapheme>
    <grapheme>wagoner</grapheme>
    <phoneme>ˈwæg.nɚ</phoneme>
  </lexeme>

  <!-- Tecumseh: "tuh-KUM-suh" -->
  <lexeme>
    <grapheme>Tecumseh</grapheme>
    <grapheme>tecumseh</grapheme>
    <phoneme>tə.ˈkʌm.sə</phoneme>
  </lexeme>

  <!-- Oologah: Birthplace of Will Rogers ("OO-luh-gah") -->
  <lexeme>
    <grapheme>Oologah</grapheme>
    <grapheme>oologah</grapheme>
    <phoneme>ˈu.lə.gɑ</phoneme>
  </lexeme>

  <!-- Checotah: "shuh-KOH-tuh" -->
  <lexeme>
    <grapheme>Checotah</grapheme>
    <grapheme>checotah</grapheme>
    <phoneme>ʃə.ˈkoʊ.tə</phoneme>
  </lexeme>

  <!-- Spiro: "SPY-roh" (Spiro Mounds) -->
  <lexeme>
    <grapheme>Spiro</grapheme>
    <grapheme>spiro</grapheme>
    <phoneme>ˈspaɪ.ɹoʊ</phoneme>
  </lexeme>

  <!-- Durant: Locally stressed on 2nd syllable "doo-RANT" -->
  <lexeme>
    <grapheme>Durant</grapheme>
    <grapheme>durant</grapheme>
    <phoneme>du.ˈɹænt</phoneme>
  </lexeme>

  <!-- Boise: In Boise City, Panhandle locals say "BOYZ" (not "boy-see") -->
  <lexeme>
    <grapheme>Boise</grapheme>
    <grapheme>boise</grapheme>
    <phoneme>ˈbɔɪz</phoneme>
  </lexeme>

  <!-- Meers: Famous burger / Wichita Mountains outpost ("MEERZ") -->
  <lexeme>
    <grapheme>Meers</grapheme>
    <grapheme>meers</grapheme>
    <phoneme>ˈmɪɹz</phoneme>
  </lexeme>

  <!-- Waurika: "waw-REE-kuh" -->
  <lexeme>
    <grapheme>Waurika</grapheme>
    <grapheme>waurika</grapheme>
    <phoneme>wɔ.ˈɹi.kə</phoneme>
  </lexeme>

  <!-- Nuyaka: "noo-YAH-kuh" -->
  <lexeme>
    <grapheme>Nuyaka</grapheme>
    <grapheme>nuyaka</grapheme>
    <phoneme>nu.ˈjɑ.kə</phoneme>
  </lexeme>

  <!-- Bowlegs: Named after Billy Bowlegs ("BOH-laygz") -->
  <lexeme>
    <grapheme>Bowlegs</grapheme>
    <grapheme>bowlegs</grapheme>
    <phoneme>ˈboʊ.leɪgz</phoneme>
  </lexeme>

  <!-- Alva: "AL-vuh" -->
  <lexeme>
    <grapheme>Alva</grapheme>
    <grapheme>alva</grapheme>
    <phoneme>ˈæl.və</phoneme>
  </lexeme>

  <!-- Coalgate: "KOLE-gate" -->
  <lexeme>
    <grapheme>Coalgate</grapheme>
    <grapheme>coalgate</grapheme>
    <phoneme>ˈkoʊl.geɪt</phoneme>
  </lexeme>

  <!-- Pocola: "poh-KOH-luh" -->
  <lexeme>
    <grapheme>Pocola</grapheme>
    <grapheme>pocola</grapheme>
    <phoneme>poʊ.ˈkoʊ.lə</phoneme>
  </lexeme>

  <!-- Washita: "WASH-ih-tah" -->
  <lexeme>
    <grapheme>Washita</grapheme>
    <grapheme>washita</grapheme>
    <phoneme>ˈwɑ.ʃɪ.tɑ</phoneme>
  </lexeme>

  <!-- Tenkiller: "TEN-kill-er" -->
  <lexeme>
    <grapheme>Tenkiller</grapheme>
    <grapheme>tenkiller</grapheme>
    <phoneme>ˈtɛn.ˌkɪl.ɚ</phoneme>
  </lexeme>

  <!-- Guymon: "GUY-mun" -->
  <lexeme>
    <grapheme>Guymon</grapheme>
    <grapheme>guymon</grapheme>
    <phoneme>ˈgaɪ.mən</phoneme>
  </lexeme>


  <!-- ================================================================= -->
  <!-- 2. REGIONAL PHONOLOGY: FOOD, FAUNA & CULTURAL VOCABULARY           -->
  <!-- ================================================================= -->

  <!-- Pecan: Always "puh-KAHN" in Oklahoma (never northern "PEE-can") -->
  <lexeme>
    <grapheme>pecan</grapheme>
    <grapheme>Pecan</grapheme>
    <phoneme>pə.ˈkɑn</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>pecans</grapheme>
    <grapheme>Pecans</grapheme>
    <phoneme>pə.ˈkɑnz</phoneme>
  </lexeme>

  <!-- Caramel: Strongly two syllables "CAR-mull" -->
  <lexeme>
    <grapheme>caramel</grapheme>
    <grapheme>Caramel</grapheme>
    <phoneme>ˈkɑɹ.məl</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>caramels</grapheme>
    <grapheme>Caramels</grapheme>
    <phoneme>ˈkɑɹ.məlz</phoneme>
  </lexeme>

  <!-- Creek: Dialectal / rural "crick" -->
  <lexeme>
    <grapheme>creek</grapheme>
    <grapheme>Creek</grapheme>
    <phoneme>ˈkɹɪk</phoneme>
  </lexeme>

  <!-- Praline: Southern "PRAW-leen" -->
  <lexeme>
    <grapheme>praline</grapheme>
    <grapheme>Praline</grapheme>
    <phoneme>ˈpɹɑ.lin</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>pralines</grapheme>
    <grapheme>Pralines</grapheme>
    <phoneme>ˈpɹɑ.linz</phoneme>
  </lexeme>

  <!-- Syrup: "SEER-up" -->
  <lexeme>
    <grapheme>syrup</grapheme>
    <grapheme>Syrup</grapheme>
    <phoneme>ˈsɪɹ.əp</phoneme>
  </lexeme>

  <!-- Crawdad / Crawdads -->
  <lexeme>
    <grapheme>crawdad</grapheme>
    <grapheme>Crawdad</grapheme>
    <phoneme>ˈkɹɔ.ˌdæd</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>crawdads</grapheme>
    <grapheme>Crawdads</grapheme>
    <phoneme>ˈkɹɔ.ˌdædz</phoneme>
  </lexeme>

  <!-- Chigger / Chiggers -->
  <lexeme>
    <grapheme>chigger</grapheme>
    <grapheme>Chigger</grapheme>
    <phoneme>ˈtʃɪ.gɚ</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>chiggers</grapheme>
    <grapheme>Chiggers</grapheme>
    <phoneme>ˈtʃɪ.gɚz</phoneme>
  </lexeme>

  <!-- Holler (valley / drawl) -->
  <lexeme>
    <grapheme>holler</grapheme>
    <grapheme>Holler</grapheme>
    <phoneme>ˈhɑ.lɚ</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>hollers</grapheme>
    <grapheme>Hollers</grapheme>
    <phoneme>ˈhɑ.lɚz</phoneme>
  </lexeme>

  <!-- Frybread -->
  <lexeme>
    <grapheme>frybread</grapheme>
    <grapheme>Frybread</grapheme>
    <phoneme>ˈfɹaɪ.ˌbɹɛd</phoneme>
  </lexeme>

  <!-- Scissortail (Oklahoma state bird) -->
  <lexeme>
    <grapheme>scissortail</grapheme>
    <grapheme>Scissortail</grapheme>
    <phoneme>ˈsɪz.ɚ.ˌteɪl</phoneme>
  </lexeme>

  <!-- Hushpuppy / Hushpuppies -->
  <lexeme>
    <grapheme>hushpuppy</grapheme>
    <grapheme>Hushpuppy</grapheme>
    <phoneme>ˈhʌʃ.ˌpʌp.i</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>hushpuppies</grapheme>
    <grapheme>Hushpuppies</grapheme>
    <phoneme>ˈhʌʃ.ˌpʌp.iz</phoneme>
  </lexeme>

  <!-- Britches -->
  <lexeme>
    <grapheme>britches</grapheme>
    <grapheme>Britches</grapheme>
    <phoneme>ˈbɹɪ.tʃɪz</phoneme>
  </lexeme>

  <!-- Bellyache -->
  <lexeme>
    <grapheme>bellyache</grapheme>
    <grapheme>Bellyache</grapheme>
    <phoneme>ˈbɛl.i.ˌeɪk</phoneme>
  </lexeme>

  <!-- Cattywampus / Catawampus -->
  <lexeme>
    <grapheme>cattywampus</grapheme>
    <grapheme>Cattywampus</grapheme>
    <grapheme>catawampus</grapheme>
    <grapheme>Catawampus</grapheme>
    <phoneme>ˌkæt.i.ˈwɑm.pəs</phoneme>
  </lexeme>

  <!-- Sooner / Sooners -->
  <lexeme>
    <grapheme>Sooner</grapheme>
    <grapheme>sooner</grapheme>
    <phoneme>ˈsu.nɚ</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>Sooners</grapheme>
    <grapheme>sooners</grapheme>
    <phoneme>ˈsu.nɚz</phoneme>
  </lexeme>

  <!-- Boomer / Boomers -->
  <lexeme>
    <grapheme>Boomer</grapheme>
    <grapheme>boomer</grapheme>
    <phoneme>ˈbu.mɚ</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>Boomers</grapheme>
    <grapheme>boomers</grapheme>
    <phoneme>ˈbu.mɚz</phoneme>
  </lexeme>

  <!-- Duster (dust storm) -->
  <lexeme>
    <grapheme>duster</grapheme>
    <grapheme>Duster</grapheme>
    <phoneme>ˈdʌs.tɚ</phoneme>
  </lexeme>


  <!-- ================================================================= -->
  <!-- 3. SOUTH MIDLAND & SOUTHERN INITIAL STRESS SHIFT                   -->
  <!-- Disyllabic nouns with initial primary stress                      -->
  <!-- ================================================================= -->

  <!-- Insurance: Dialectal initial stress "IN-shur-unce" -->
  <lexeme>
    <grapheme>insurance</grapheme>
    <grapheme>Insurance</grapheme>
    <phoneme>ˈɪn.ʃʊɹ.əns</phoneme>
  </lexeme>

  <!-- Umbrella: Dialectal initial stress "UM-brel-luh" -->
  <lexeme>
    <grapheme>umbrella</grapheme>
    <grapheme>Umbrella</grapheme>
    <phoneme>ˈʌm.bɹɛl.ə</phoneme>
  </lexeme>

  <!-- Police: Dialectal initial stress "PO-leece" -->
  <lexeme>
    <grapheme>police</grapheme>
    <grapheme>Police</grapheme>
    <phoneme>ˈpoʊ.lis</phoneme>
  </lexeme>

  <!-- Cement: Dialectal initial stress "SEE-ment" -->
  <lexeme>
    <grapheme>cement</grapheme>
    <grapheme>Cement</grapheme>
    <phoneme>ˈsi.mɛnt</phoneme>
  </lexeme>

  <!-- Guitar: Dialectal initial stress "GIT-tar" -->
  <lexeme>
    <grapheme>guitar</grapheme>
    <grapheme>Guitar</grapheme>
    <phoneme>ˈgɪ.tɑɹ</phoneme>
  </lexeme>

  <!-- Thanksgiving: Dialectal initial stress "THANKS-giv-ing" -->
  <lexeme>
    <grapheme>Thanksgiving</grapheme>
    <grapheme>thanksgiving</grapheme>
    <phoneme>ˈθæŋks.ˌgɪv.ɪŋ</phoneme>
  </lexeme>

  <!-- Detroit: Dialectal initial stress "DEE-troit" -->
  <lexeme>
    <grapheme>Detroit</grapheme>
    <grapheme>detroit</grapheme>
    <phoneme>ˈdi.tɹɔɪt</phoneme>
  </lexeme>

  <!-- Vehicle: Dialectal aspirated 'h' and strong initial stress "VEE-hick-ul" -->
  <lexeme>
    <grapheme>vehicle</grapheme>
    <grapheme>Vehicle</grapheme>
    <phoneme>ˈvi.hɪk.əl</phoneme>
  </lexeme>


  <!-- ================================================================= -->
  <!-- 4. MIDLAND INTRUSIVE 'R' ("WARSH" PHENOMENON)                     -->
  <!-- Common in rural and traditional Midland Oklahoma speech           -->
  <!-- ================================================================= -->

  <!-- Wash -> "warsh" -->
  <lexeme>
    <grapheme>wash</grapheme>
    <grapheme>Wash</grapheme>
    <phoneme>wɑɹʃ</phoneme>
  </lexeme>

  <!-- Washing -> "warshing" -->
  <lexeme>
    <grapheme>washing</grapheme>
    <grapheme>Washing</grapheme>
    <phoneme>ˈwɑɹ.ʃɪŋ</phoneme>
  </lexeme>

  <!-- Washer -> "warsher" -->
  <lexeme>
    <grapheme>washer</grapheme>
    <grapheme>Washer</grapheme>
    <phoneme>ˈwɑɹ.ʃɚ</phoneme>
  </lexeme>

  <!-- Washington -> "Warshington" -->
  <lexeme>
    <grapheme>Washington</grapheme>
    <grapheme>washington</grapheme>
    <phoneme>ˈwɑɹ.ʃɪŋ.tən</phoneme>
  </lexeme>


  <!-- ================================================================= -->
  <!-- 5. PIN-PEN MERGER & /aɪ/ MONOPHTHONGIZATION (RURAL TRAITS)        -->
  <!-- ================================================================= -->

  <!-- Pen / Pin merger -->
  <lexeme>
    <grapheme>pen</grapheme>
    <grapheme>Pen</grapheme>
    <phoneme>pɪn</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>pencil</grapheme>
    <grapheme>Pencil</grapheme>
    <phoneme>ˈpɪn.səl</phoneme>
  </lexeme>
  <lexeme>
    <grapheme>fence</grapheme>
    <grapheme>Fence</grapheme>
    <phoneme>fɪns</phoneme>
  </lexeme>

  <!-- Monophthongization of /aɪ/ before /r/: fire -> "fahr" -->
  <lexeme>
    <grapheme>fire</grapheme>
    <grapheme>Fire</grapheme>
    <phoneme>fɑɹ</phoneme>
  </lexeme>

  <!-- tire -> "tahr" -->
  <lexeme>
    <grapheme>tire</grapheme>
    <grapheme>Tire</grapheme>
    <phoneme>tɑɹ</phoneme>
  </lexeme>

  <!-- wire -> "wahr" -->
  <lexeme>
    <grapheme>wire</grapheme>
    <grapheme>Wire</grapheme>
    <phoneme>wɑɹ</phoneme>
  </lexeme>


  <!-- ================================================================= -->
  <!-- 6. COLLOQUIAL TERMS, CONTRACTIONS & MULTI-WORD IDIOMS             -->
  <!-- ================================================================= -->

  <!-- Y'all -->
  <lexeme>
    <grapheme>y'all</grapheme>
    <grapheme>Y'all</grapheme>
    <grapheme>yall</grapheme>
    <grapheme>Yall</grapheme>
    <phoneme>jɔl</phoneme>
  </lexeme>

  <!-- Fixin' / Fixin -->
  <lexeme>
    <grapheme>fixin'</grapheme>
    <grapheme>Fixin'</grapheme>
    <grapheme>fixin</grapheme>
    <grapheme>Fixin</grapheme>
    <phoneme>ˈfɪk.sən</phoneme>
  </lexeme>

  <!-- Multi-word phrase: fixin' to -> fixinto -->
  <lexeme>
    <grapheme>fixin' to</grapheme>
    <grapheme>Fixin' to</grapheme>
    <grapheme>fixin to</grapheme>
    <grapheme>Fixin to</grapheme>
    <alias>fixinto</alias>
  </lexeme>
  <lexeme>
    <grapheme>fixinto</grapheme>
    <phoneme>ˈfɪk.sən.tu</phoneme>
  </lexeme>

  <!-- Yonder -->
  <lexeme>
    <grapheme>yonder</grapheme>
    <grapheme>Yonder</grapheme>
    <phoneme>ˈjɑn.dɚ</phoneme>
  </lexeme>

  <!-- Multi-word phrase: over yonder -> overyonder -->
  <lexeme>
    <grapheme>over yonder</grapheme>
    <grapheme>Over yonder</grapheme>
    <alias>overyonder</alias>
  </lexeme>
  <lexeme>
    <grapheme>overyonder</grapheme>
    <phoneme>ˈoʊ.vɚ.ˈjɑn.dɚ</phoneme>
  </lexeme>

  <!-- Multi-word phrase: Boise City -> BoiseCity -->
  <lexeme>
    <grapheme>Boise City</grapheme>
    <grapheme>boise city</grapheme>
    <alias>BoiseCity</alias>
  </lexeme>
  <lexeme>
    <grapheme>BoiseCity</grapheme>
    <phoneme>ˈbɔɪz.ˈsɪ.ti</phoneme>
  </lexeme>

  <!-- Multi-word phrase: frog strangler (torrential rain) -->
  <lexeme>
    <grapheme>frog strangler</grapheme>
    <grapheme>frog-strangler</grapheme>
    <alias>frogstrangler</alias>
  </lexeme>
  <lexeme>
    <grapheme>frogstrangler</grapheme>
    <phoneme>ˈfɹɑg.ˌstɹæŋ.glɚ</phoneme>
  </lexeme>

  <!-- Multi-word phrase: gully washer -->
  <lexeme>
    <grapheme>gully washer</grapheme>
    <grapheme>gully-washer</grapheme>
    <alias>gullywasher</alias>
  </lexeme>
  <lexeme>
    <grapheme>gullywasher</grapheme>
    <phoneme>ˈgʌl.i.ˌwɑɹ.ʃɚ</phoneme>
  </lexeme>

  <!-- Multi-word phrase: roasting ears (corn on the cob) -->
  <lexeme>
    <grapheme>roasting ears</grapheme>
    <grapheme>roastin' ears</grapheme>
    <grapheme>roastin ears</grapheme>
    <alias>roastinears</alias>
  </lexeme>
  <lexeme>
    <grapheme>roastinears</grapheme>
    <phoneme>ˈɹoʊs.tɪn.ɪɹz</phoneme>
  </lexeme>

  <!-- Multi-word phrase: all get out -->
  <lexeme>
    <grapheme>all get out</grapheme>
    <grapheme>All get out</grapheme>
    <alias>allgetout</alias>
  </lexeme>
  <lexeme>
    <grapheme>allgetout</grapheme>
    <phoneme>ˈɔl.gɪt.ˈaʊt</phoneme>
  </lexeme>

</lexicon>
```

---

## 3. Linguistic Rationale & Dialect Breakdown

### A. Indigenous & Regional Toponyms
Standard neural Text-to-Speech models are trained on general American English data. Oklahoma has **39 federally recognized tribal nations**, resulting in town, river, and landmark names derived from Muscogee Creek, Cherokee, Choctaw, Chickasaw, Seminole, Osage, Kiowa, and Delaware (Lenape) roots. Furthermore, European settlement patterns produced unique local pronunciations:
- **Prague**: Known throughout the state as `ˈpɹeɪg` ("PRAYG"), rhyming with *vague*, settled by Czech immigrants.
- **Miami**: Overwhelmingly `maɪ.ˈæ.mə` ("my-AM-uh"), derived from the Miami Tribe.
- **Chickasha**: Consistently `ˈtʃɪk.ə.ʃeɪ` ("CHICK-uh-shay"), named after the Chickasaw.
- **Nowata**: Lenape *nuwita* pronounced `noʊ.ˈweɪ.tə` ("no-WAY-tuh").
- **Boise City**: In the Oklahoma Panhandle, locals pronounce Boise as `ˈbɔɪz` ("Boyz"), rather than the Idaho pronunciation `ˈbɔɪ.si`.

### B. South Midland Initial Stress Shift
In Oklahoma English (consistent with the South Midland dialect zone), words that carry second-syllable stress in General American English regularly shift primary stress to the first syllable:
- *insurance* -> `ˈɪn.ʃʊɹ.əns` ("IN-shur-unce")
- *police* -> `ˈpoʊ.lis` ("PO-leece")
- *umbrella* -> `ˈʌm.bɹɛl.ə` ("UM-brel-luh")
- *cement* -> `ˈsi.mɛnt` ("SEE-ment")
- *guitar* -> `ˈgɪ.tɑɹ` ("GIT-tar")

### C. Phonological Traits: Intrusive 'R', Monophthongization & Pin-Pen
- **Intrusive R ("Warsh")**: Characteristic of older, rural Midland and Ozark-influenced Oklahoma English (`wɑɹʃ`, `ˈwɑɹ.ʃɪŋ.tən`).
- **Pin-Pen Merger**: Front lax vowels before nasals merge to `/ɪ/`, making *pen* sound identical to *pin* (`pɪn`), *fence* to `fɪns`.
- **Monophthongization of /aɪ/ before /r/**: Diphthong reduction turns *fire* into `fɑɹ` ("fahr"), *tire* into `tɑɹ`, and *wire* into `wɑɹ`.
- **Pecan / Caramel**: *Pecan* is strictly `pə.ˈkɑn` ("puh-KAHN"), and *caramel* is two syllables `ˈkɑɹ.məl` ("CAR-mull").

### D. Multi-Word Phrasing in Azure Custom Lexicon
Azure AI Speech enforces a specific constraint: **`<phoneme>` cannot be applied directly to a multi-word phrase**. The official Microsoft architecture requires mapping the multi-word grapheme to a single token using `<alias>`, and then defining the `<phoneme>` for that token:
```xml
<lexeme>
  <grapheme>over yonder</grapheme>
  <alias>overyonder</alias>
</lexeme>
<lexeme>
  <grapheme>overyonder</grapheme>
  <phoneme>ˈoʊ.vɚ.ˈjɑn.dɚ</phoneme>
</lexeme>
```

---

## 4. Testing & Validation Checklist

1. **W3C PLS 1.0 Validation**: Check that the root element is `<lexicon>` with `version="1.0"`, `alphabet="ipa"`, and `xml:lang="en-US"`.
2. **Phone Validation**: All IPA characters adhere strictly to Azure's supported phone set for `en-US` (` speech-ssml-phonetic-sets.md`). Unrecognized phones cause an HTTP 400 bad request.
3. **Case Sensitivity**: Azure Speech grapheme matching is case-sensitive. The lexicon entries explicitly declare both capitalized and lowercase forms.
4. **Cache Invalidation**: Azure caches remote custom lexicons for approximately **15 minutes**. When updating, change the query string (e.g. `?v=2`) or wait 15 minutes.
5. **File Size**: At ~15 KB, this file is well below Azure's 100 KB limit for custom lexicons.
