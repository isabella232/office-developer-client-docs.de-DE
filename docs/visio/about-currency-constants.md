---
title: Informationen zu Währungskonstanten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82253123
ms.localizationpriority: medium
ms.assetid: d94c740f-29e1-1e7f-39f6-8aa215f3111d
description: Um eine Zahl als Währung zu formatieren, können Sie die CY-Funktion verwenden und eine optionale Konstante übergeben, um anzugeben, welches Land/welche Region die Währung verwenden soll. Die Währungskonstanten können als ID-Nummer angegeben werden, die einem Land/einer Region entspricht, oder als Zeichenfolge (in Anführungszeichen eingeschlossen), die einer dreistelligen ISO 4217-Abkürzung entspricht.
ms.openlocfilehash: 17e559e9c2cdc2a09ce437af5918ce4457b144dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608760"
---
# <a name="about-currency-constants"></a>Informationen zu Währungskonstanten

Um eine Zahl als Währung zu formatieren, können Sie die CY-Funktion verwenden und eine optionale Konstante übergeben, um anzugeben, welches Land/welche Region die Währung verwenden soll. Die Währungskonstanten können als ID-Nummer angegeben werden, die einem Land/einer Region entspricht, oder als Zeichenfolge (in Anführungszeichen eingeschlossen), die einer dreistelligen ISO 4217-Abkürzung entspricht.
  
Wenn Sie Währungssymbole für nicht lokale Währungen anzeigen und das System das Symbol für eine bestimmte Währung nicht kennt, wird das Dollarsymbol ($) angezeigt.
  
## <a name="ids-and-abbreviations"></a>IDs und Abkürzungen

|**ID**|**Abbreviation**|**Currency**|
|:-----|:-----|:-----|
| 0  <br/> | SYS  <br/> | Verwendet Systemeinstellungen  <br/> |
| 1  <br/> | XXX  <br/> | Formate als Zahl  <br/> |
| 2 - 9  <br/> | Reserved  <br/> |
| 10  <br/> | EUR  <br/> | Euro  <br/> |
| 11  <br/> | USD  <br/> | US-Dollar  <br/> |
| 12   <br/> | ATS  <br/> | Wiesn Schilling  <br/> |
| 13  <br/> | AUD  <br/> | Australischer Dollar  <br/> |
| 14   <br/> | BEF  <br/> | Belgien (Frankreich)  <br/> |
| 15   <br/> | CAD  <br/> | Kanadischer Dollar  <br/> |
| 16   <br/> | CHF  <br/> | Swiss Franc  <br/> |
| 17   <br/> | CNY  <br/> | Chinese Yuan Renminbi  <br/> |
| 18   <br/> | DEM  <br/> | Deutsche Mark  <br/> |
| 19  <br/> | DKK  <br/> | Dänische Kronen  <br/> |
| 20  <br/> | ESP  <br/> | Spanisch (Peseta)  <br/> |
|  21  <br/> | FIM  <br/> | Finnische Mark  <br/> |
| 22  <br/> | FRF  <br/> | Französisch (Frankreich)  <br/> |
| 23  <br/> | GBP  <br/> | Britisches Britisches Britisches Kilo  <br/> |
| 24  <br/> | GRD  <br/> | Griechisch Drachme  <br/> |
| 25  <br/> | HKD  <br/> | Sonderverwaltungsregion Hongkong (SAR) Dollar  <br/> |
| 26  <br/> | HUF  <br/> | Ungarn Forint  <br/> |
| 27  <br/> | IDR  <br/> | Indonesische Rupiah  <br/> |
| 28  <br/> | IEP  <br/> | Irish Punt  <br/> |
| 29  <br/> | ILS  <br/> | Scheikel  <br/> |
| 30  <br/> | ITL  <br/> | Italienisch Lira  <br/> |
| 31  <br/> | JPY  <br/> | Japanisch(n)  <br/> |
| 32  <br/> | KRW  <br/> | Koreanisch (Won)  <br/> |
| 33  <br/> | LUF  <br/> | Luxemburgisch (Frankreich)  <br/> |
| 34  <br/> | MXN  <br/> | Mexican Peso  <br/> |
| 35  <br/> | MYR  <br/> | Malaysian Ringgit  <br/> |
| 36  <br/> | NLG  <br/> | Niederländisch(n)  <br/> |
| 37  <br/> | NOK  <br/> | Norwegisch(n)  <br/> |
| 38  <br/> | NZD  <br/> | Neuseeland-Dollar  <br/> |
| 39  <br/> | PHP  <br/> | Philippinen Peso  <br/> |
| 40  <br/> | PLZ (Historisches Plz. Verwenden Sie PLN.)  <br/> | Polish Zloty  <br/> |
| 41  <br/> | PTE  <br/> | Portugiesisch (Dotdo)  <br/> |
| 42  <br/> | ROL  <br/> | Rumänisch Leu  <br/> |
| 43  <br/> | RUR (Historisches. Verwenden Sie RUB.)  <br/> | Russisch (Russisch)  <br/> |
| 44  <br/> | SEK  <br/> | Schwedisch-Seker  <br/> |
| 45  <br/> | SGD  <br/> | Singapur-Dollar  <br/> |
| 46  <br/> | THB  <br/> | Thailändisch (Thailändisch)  <br/> |
| 47  <br/> | TWD  <br/> | Neuer Taiwan-Dollar  <br/> |
| 48  <br/> | XEU (Historisches. Verwenden Sie EUR.)  <br/> | MAUSTASTE (vor 1998)  <br/> |
| 49  <br/> | YUN (Historisches. Verwenden Sie YUM.)  <br/> | Dinar (Enthingen)  <br/> |
| 50  <br/> | ZAR  <br/> | Rand des Südostens  <br/> |
| 51 - 55  <br/> | Reserved  <br/> |
| 56  <br/> | ARS  <br/> | Argentiniens Peso  <br/> |
| 57  <br/> | BMD  <br/> | Bermudian Dollar  <br/> |
| 58  <br/> | BOB  <br/> | Peruanisch (Bolivien)  <br/> |
| 59  <br/> | BRR (Historisches. Verwenden Sie BRL.)  <br/> | Brasilianischer Uhriero Real  <br/> |
| 60  <br/> | BSD  <br/> | Bahamanien-Dollar  <br/> |
| 61  <br/> | CLP  <br/> | Chilenischer Peso  <br/> |
| 62  <br/> | COP  <br/> | Kolumbiens Peso  <br/> |
| 63  <br/> | CRC  <br/> | Costa Ricon Colon  <br/> |
| 64  <br/> | CZK  <br/> | Tschechische Koruna  <br/> |
| 65  <br/> | DOP  <br/> | Dominikanischer Peso  <br/> |
| 66  <br/> | ECS  <br/> | Ecuadorean Sucre  <br/> |
| 67  <br/> | EGP  <br/> | Britisches Kilo  <br/> |
| 68  <br/> | HNL  <br/> | Honduran Lempira  <br/> |
| 69  <br/> | INR  <br/> | Indien Rupe  <br/> |
| 70  <br/> | JMD  <br/> | Dollar (Aufrhöher)  <br/> |
| 71  <br/> | JOD  <br/> | Jordanischer Dinar  <br/> |
| 72  <br/> | KWD  <br/> | Omani Dinar  <br/> |
| 73  <br/> | MOP  <br/> | Macanese Pataca  <br/> |
| 74  <br/> | NIO  <br/> | Nicaraguan Coexisten Oro  <br/> |
| 75  <br/> | PAB  <br/> | Balboa (Panama)  <br/> |
| 76  <br/> | STIFT  <br/> | Peruvian Nuevo Sol  <br/> |
| 77  <br/> | PKR  <br/> | Pakistani Rupee  <br/> |
| 78  <br/> | PYG  <br/> | Paraguayisch-Gurani  <br/> |
| 79  <br/> | SAR  <br/> | Saudi Riyal  <br/> |
| 80  <br/> | SITZEN  <br/> | Slowenisch-Tolar  <br/> |
| 81  <br/> | SKK  <br/> | Slowakisch Koruna  <br/> |
| 82  <br/> | SVC  <br/> | El Salvadoran Colon  <br/> |
| 83  <br/> | VERSUCHEN  <br/> | Neue Türkisch Lira  <br/> |
| 84  <br/> | TTD  <br/> | Trinidad und Tobago Dollar  <br/> |
| 85  <br/> | UYU  <br/> | Paraguayan Peso Paraguayo  <br/> |
| 86  <br/> | VEB  <br/> | Venezuelan Bolivar  <br/> |
| 87  <br/> | VND  <br/> | Vietnamesisch(Vietnamesisch)  <br/> |
| 88  <br/> | BRL  <br/> | Brasilianischer Real  <br/> |
| 89  <br/> | PLN  <br/> | Polish Zloty  <br/> |
| 90  <br/> | REIBEN  <br/> | Russisch (Russisch)  <br/> |
| 91  <br/> | LECKER  <br/> | Dinar (Enthingen)  <br/> |
| 92  <br/> | BYB (Historisches Objekt. Verwenden Sie BYR.)  <br/> | Weißrussisch (Borussisch)  <br/> |
| 93  <br/> | UAH  <br/> | Ukrainisch Hryvnia  <br/> |
| 94  <br/> | AFA  <br/> | I (hinzugefügt in Visio 2002)  <br/> |
| 95  <br/> | ALLE  <br/> | Lek (hinzugefügt in Visio 2002)  <br/> |
| 96  <br/> | DZD  <br/> | Algerischer Dinar (hinzugefügt in Visio 2002)  <br/> |
| 97  <br/> | ADP  <br/> | Andorran Peseta (hinzugefügt in Visio 2002)  <br/> |
| 98  <br/> | AOA  <br/> | Kwanza (hinzugefügt in Visio 2002)  <br/> |
| 99  <br/> | XCD  <br/> | East -Dollar (hinzugefügt in Visio 2002)  <br/> |
| 100  <br/> | AMD  <br/> | Armenischer Dram (hinzugefügt in Visio 2002)  <br/> |
| 101  <br/> | AWG  <br/> | Dies ist ein in Visio 2002 hinzugefügtes Element.  <br/> |
| 102  <br/> | AZM  <br/> | Aserbaidschanischer Manat (hinzugefügt in Visio 2002)  <br/> |
| 103  <br/> | BHD  <br/> | Kuwaiti Dinar (hinzugefügt in Visio 2002)  <br/> |
| 104  <br/> | BDT  <br/> | Doppelklick (hinzugefügt in Visio 2002)  <br/> |
| 105  <br/> | BBD  <br/> | Dollar (hinzugefügt in Visio 2002)  <br/> |
| 106  <br/> | BYR  <br/> | Weißrussisch (hinzugefügt in Visio 2002)  <br/> |
| 107  <br/> | BZD  <br/> | Belize-Dollar (hinzugefügt in Visio 2002)  <br/> |
| 108  <br/> | XOF  <br/> | CFA Franc BCEAO (hinzugefügt in Visio 2002)  <br/> |
| 109  <br/> | BTN  <br/> | Ngultrum (hinzugefügt in Visio 2002)  <br/> |
| 110  <br/> | BAM  <br/> | Konvertierbare Markierungen (hinzugefügt in Visio 2002)  <br/> |
| 111  <br/> | BWP  <br/> | Pula (hinzugefügt in Visio 2002)  <br/> |
| 112  <br/> | BND  <br/> | Brunei Dollar (hinzugefügt in Visio 2002)  <br/> |
| 113  <br/> | BGL (Historisches. Verwenden Sie BGN.)  <br/> | Lev  <br/> |
| 114  <br/> | BGN  <br/> | Bulgarisch-Lev (hinzugefügt in Visio 2002)  <br/> |
| 115  <br/> | BIF  <br/> | Doppelklicken (hinzugefügt in Visio 2002)  <br/> |
| 116  <br/> | KHR  <br/> | Riel (hinzugefügt in Visio 2002)  <br/> |
| 117  <br/> | XAF  <br/> | CFA-Franc BEAC (hinzugefügt in Visio 2002)  <br/> |
| 118  <br/> | CVE  <br/> | Cabo Verde Ausdo (hinzugefügt in Visio 2002)  <br/> |
| 119  <br/> | KYD  <br/> | Cayman Islands Dollar (hinzugefügt in Visio 2002)  <br/> |
| 120  <br/> | KMF  <br/> | Comoro Franc (hinzugefügt in Visio 2002)  <br/> |
| 121  <br/> | CDF  <br/> | Franc Congolais (hinzugefügt in Visio 2002)  <br/> |
| 122  <br/> | HRK  <br/> | Kuna (hinzugefügt in Visio 2002)  <br/> |
| 123  <br/> | TASSE  <br/> | Peso (hinzugefügt in Visio 2002)  <br/> |
| 124  <br/> | CYP  <br/> | Britisches Kilo (hinzugefügt in Visio 2002)  <br/> |
| 125  <br/> | DJF  <br/> | Francbouti Franc (hinzugefügt in Visio 2002)  <br/> |
| 126  <br/> | TPE  <br/> | Codier-Dosdo (hinzugefügt in Visio 2002)  <br/> |
| 127  <br/> | ERN  <br/> | Nakfa (hinzugefügt in Visio 2002)  <br/> |
| 128  <br/> | EEK  <br/> | Kroon (hinzugefügt in Visio 2002)  <br/> |
| 129  <br/> | ETB  <br/> | Der äthiopische Birr (hinzugefügt in Visio 2002)  <br/> |
| 130  <br/> | FKP  <br/> | Islands (Islas Malvinas) Pound (added in Visio 2002)  <br/> |
| 131  <br/> | FJD  <br/> | Fidschi-Dollar (hinzugefügt in Visio 2002)  <br/> |
| 132  <br/> | XPF  <br/> | CFP-Franc (hinzugefügt in Visio 2002)  <br/> |
| 133  <br/> | GMD  <br/> | Dalasi (hinzugefügt in Visio 2002)  <br/> |
| 134  <br/> | GEL  <br/> | Lari (hinzugefügt in Visio 2002)  <br/> |
| 135  <br/> | GHC  <br/> | Cedi (hinzugefügt in Visio 2002)  <br/> |
| 136  <br/> | GIP  <br/> | Doppelklicken (hinzugefügt in Visio 2002)  <br/> |
| 137  <br/> | GTQ  <br/> | Quetzal (hinzugefügt in Visio 2002)  <br/> |
| 138  <br/> | GNF  <br/> | Guinea-Franc (hinzugefügt in Visio 2002)  <br/> |
| 139  <br/> | GWP  <br/> | Guinea-Bissau Peso (hinzugefügt in Visio 2002)  <br/> |
| 140  <br/> | GYD  <br/> | Codana Dollar (hinzugefügt in Visio 2002)  <br/> |
| 141  <br/> | HTG  <br/> | Gourde (hinzugefügt in Visio 2002)  <br/> |
| 142  <br/> | ISK  <br/> | Island (hinzugefügt in Visio 2002)  <br/> |
| 143  <br/> | IKV  <br/> | Riad Rial (hinzugefügt in Visio 2002)  <br/> |
| 144  <br/> | IQD  <br/> | Aufzählungs dinar (hinzugefügt in Visio 2002)  <br/> |
| 145  <br/> | KZT  <br/> | Tenge (hinzugefügt in Visio 2002)  <br/> |
| 146  <br/> | KES  <br/> | Kennianisches S codieren (hinzugefügt in Visio 2002)  <br/> |
| 147  <br/> | KPW  <br/> | North Korean Won (added in Visio 2002)  <br/> |
| 148  <br/> | KG  <br/> | Som (hinzugefügt in Visio 2002)  <br/> |
| 149  <br/> | LAK  <br/> | Kip (hinzugefügt in Visio 2002)  <br/> |
| 150  <br/> | LVL (Historisches. Verwenden Sie EUR.)  <br/> | Lettisch Lats (hinzugefügt in Visio 2002)  <br/> |
| 151  <br/> | LBP  <br/> | Pound (hinzugefügt in Visio 2002)  <br/> |
| 152  <br/> | LSL  <br/> | Loti (hinzugefügt in Visio 2002)  <br/> |
| 153  <br/> | LRD  <br/> | Dollar (hinzugefügt in Visio 2002)  <br/> |
| 154  <br/> | LYD  <br/> | Der libysche Dinar (hinzugefügt in Visio 2002)  <br/> |
| 155  <br/> | LTL  <br/> | Litus in Litauisch (hinzugefügt in Visio 2002)  <br/> |
| 156  <br/> | MKD  <br/> | Denar (hinzugefügt in Visio 2002)  <br/> |
| 157  <br/> | MGF (Historisches. Verwenden Sie MGA.)  <br/> | 2002: 2002 Visio hinzugefügt  <br/> |
| 158  <br/> | MWK  <br/> | Paraguayan Doppelklickcha (hinzugefügt in Visio 2002)  <br/> |
| 159  <br/> | MVR  <br/> | Rufijaa (hinzugefügt in Visio 2002)  <br/> |
| 160  <br/> | MTL  <br/> | Doppelklick lira (hinzugefügt in Visio 2002)  <br/> |
| 161  <br/> | MRO  <br/> | Ouguiya (hinzugefügt in Visio 2002)  <br/> |
| 162  <br/> | MUR  <br/> | Mauritius Rupee (hinzugefügt in Visio 2002)  <br/> |
| 163  <br/> | MDL  <br/> | Moldovan Leu (hinzugefügt in Visio 2002)  <br/> |
| 164  <br/> | MNT  <br/> | Tugrik (hinzugefügt in Visio 2002)  <br/> |
| 165  <br/> | WÜTEND  <br/> | Die Dirham-Methode (hinzugefügt in Visio 2002)  <br/> |
| 166  <br/> | MZM  <br/> | Metical (hinzugefügt in Visio 2002)  <br/> |
| 167  <br/> | MMK  <br/> | Kyat (hinzugefügt in Visio 2002)  <br/> |
| 168  <br/> | NAD  <br/> | Codiert dollar (hinzugefügt in Visio 2002)  <br/> |
| 169  <br/> | NPR  <br/> | Nepalesische Rupee (hinzugefügt in Visio 2002)  <br/> |
| 170  <br/> | ANG  <br/> | Netherlands AntillianHiber (added in Visio 2002)  <br/> |
| 171  <br/> | NGN  <br/> | Naira (hinzugefügt in Visio 2002)  <br/> |
| 172  <br/> | OMR  <br/> | Rial Omani (hinzugefügt in Visio 2002)  <br/> |
| 173  <br/> | PGK  <br/> | Kina (hinzugefügt in Visio 2002)  <br/> |
| 174  <br/> | QAR  <br/> | Marshalli Rial (hinzugefügt in Visio 2002)  <br/> |
| 175  <br/> | RWF  <br/> | Franc (hinzugefügt in Visio 2002)  <br/> |
| 176  <br/> | SHP  <br/> | St. Paul Pound (hinzugefügt in Visio 2002)  <br/> |
| 177  <br/> | WST  <br/> | Tala (hinzugefügt in Visio 2002)  <br/> |
| 178  <br/> | STD  <br/> | Dobra (hinzugefügt in Visio 2002)  <br/> |
| 179  <br/> | SCR  <br/> | Rupee (hinzugefügt in Visio 2002)  <br/> |
| 180  <br/> | SLL  <br/> | Sierra (hinzugefügt in Visio 2002)  <br/> |
| 181  <br/> | SBD  <br/> | Solomon Islands Dollar (hinzugefügt in Visio 2002)  <br/> |
| 182  <br/> | SOS  <br/> | Doppelklicken (hinzugefügt in Visio 2002)  <br/> |
| 183  <br/> | LKR  <br/> | Sri Lanka Rupee (hinzugefügt in Visio 2002)  <br/> |
| 184  <br/> | SDD  <br/> | Baskischer Dinar (hinzugefügt in Visio 2002)  <br/> |
| 185  <br/> | SRG  <br/> | Suriname-Gerüst (hinzugefügt in Visio 2002)  <br/> |
| 186  <br/> | SZL  <br/> | Liungni (hinzugefügt in Visio 2002)  <br/> |
| 187  <br/> | SYP  <br/> | Pound (added in Visio 2002)  <br/> |
| 188  <br/> | TJR (Historisches. Verwenden Sie TJS.)  <br/> | Tadschikisch ( 1993)  <br/> |
| 189  <br/> | TJS  <br/> | Tadschik Somoni (hinzugefügt in Visio 2002)  <br/> |
| 190  <br/> | TZS  <br/> | Tannisch-S aus der Welt (hinzugefügt in Visio 2002)  <br/> |
| 191  <br/> | NACH OBEN  <br/> | Pa'anga (hinzugefügt in Visio 2002)  <br/> |
| 192  <br/> | TND  <br/> | Tunesisch Dinar (hinzugefügt in Visio 2002)  <br/> |
| 193  <br/> | TMM  <br/> | Manat (hinzugefügt in Visio 2002)  <br/> |
| 194  <br/> | UGX  <br/> | 1993 (hinzugefügt in Visio 2002)  <br/> |
| 195  <br/> | AED  <br/> | UAE Dirham (hinzugefügt in Visio 2002)  <br/> |
| 196  <br/> | UZS  <br/> | Sum (hinzugefügt in Visio 2002)  <br/> |
| 197  <br/> | VUV  <br/> | Vatu (hinzugefügt in Visio 2002)  <br/> |
| 198  <br/> | YER  <br/> | Ein rial (hinzugefügt in Visio 2002)  <br/> |
| 199  <br/> | ZMK  <br/> | Dies ist der in Visio 2002 hinzugefügte".  <br/> |
| 200  <br/> | ZWD  <br/> | Dollar für Dollar in Der Dollar (hinzugefügt in Visio 2002)  <br/> |
|201  <br/> |VEF  <br/> |Venezuelan Bolivar Fuente (hinzugefügt in Visio 2010)  <br/> |
|202  <br/> |MGA  <br/> |Ariary (hinzugefügt in Visio 2010)  <br/> |
|203  <br/> |RSD  <br/> |Serbisch Dinar (hinzugefügt in Visio 2010)  <br/> |
|204  <br/> |CSD (Historisches Objekt. Rsd verwenden.)  <br/> |Serbisch Dinar (hinzugefügt in Visio 2010)  <br/> |
   

