---
title: Informationen zu Währungskonstanten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82253123
localization_priority: Normal
ms.assetid: d94c740f-29e1-1e7f-39f6-8aa215f3111d
description: Wenn Sie eine Zahl als Währung formatieren möchten, können Sie die CY-Funktion verwenden und eine optionale Konstante angeben, um anzugeben, welche Landes-/Regions Währung verwendet werden soll. Die Währungskonstanten können als ID-Nummer angegeben werden, die einem Land/einer Region entspricht, oder als Zeichenfolge (in Anführungszeichen eingeschlossen), die einer ISO 4217 3-Zeichen Abkürzung entspricht.
ms.openlocfilehash: 4492f4901779d94a32b881c973eab9e32a9c0514
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421795"
---
# <a name="about-currency-constants"></a>Informationen zu Währungskonstanten

Wenn Sie eine Zahl als Währung formatieren möchten, können Sie die CY-Funktion verwenden und eine optionale Konstante angeben, um anzugeben, welche Landes-/Regions Währung verwendet werden soll. Die Währungskonstanten können als ID-Nummer angegeben werden, die einem Land/einer Region entspricht, oder als Zeichenfolge (in Anführungszeichen eingeschlossen), die einer ISO 4217 3-Zeichen Abkürzung entspricht.
  
Wenn Sie Währungssymbole für nicht lokale Währungen anzeigen und das System das Symbol für eine bestimmte Währung nicht kennt, wird das Dollar Symbol ($) angezeigt.
  
## <a name="ids-and-abbreviations"></a>IDs und Abkürzungen

|**ID**|**Abbreviation**|**Currency**|
|:-----|:-----|:-----|
| 0  <br/> | SYS  <br/> | Verwendet Systemeinstellungen  <br/> |
| 1  <br/> | XXX  <br/> | Formate als Zahl  <br/> |
| 2-9  <br/> | Reserved  <br/> |
| 10   <br/> | EUR  <br/> | Euro  <br/> |
| 11   <br/> | USD  <br/> | US-Dollar  <br/> |
| 12  <br/> | ATS  <br/> | Österreichische Schilling  <br/> |
| 13   <br/> | Wert AUD  <br/> | Australischer Dollar  <br/> |
| 14   <br/> | BEF  <br/> | Belgischer Franken  <br/> |
| 15   <br/> | CAD  <br/> | Kanadischer Dollar  <br/> |
| 16   <br/> | CHF  <br/> | Schweizer Franken  <br/> |
| 17  <br/> | CNY  <br/> | Renminbi (Yuan)  <br/> |
| 18  <br/> | DEM  <br/> | Deutsches Zeichen  <br/> |
| 19  <br/> | DKK  <br/> | Dänische Kronen  <br/> |
| 20  <br/> | ESP  <br/> | Spanisch Peseten  <br/> |
| 21  <br/> | FIM  <br/> | Finnische Mark  <br/> |
| 22  <br/> | FRF  <br/> | Französischer Franken  <br/> |
| 23  <br/> | GBP  <br/> | Britisches Pfund Sterling  <br/> |
| 24  <br/> | GRD  <br/> | Griechische Drachme  <br/> |
| 25  <br/> | HKD  <br/> | Hong Kong Special Administrative Region (SAR)-Dollar  <br/> |
| 26  <br/> | HUF  <br/> | Ungarisch Forint  <br/> |
| 27  <br/> | IDR  <br/> | Indonesische Rupiah  <br/> |
| 28  <br/> | IEP  <br/> | Irischer Punt  <br/> |
| 29  <br/> | ILS  <br/> | Israelischer Schekel  <br/> |
| 30  <br/> | ITL  <br/> | Italienische Lira  <br/> |
| 31  <br/> | JPY  <br/> | Japanischer Yen  <br/> |
| 32  <br/> | KRW  <br/> | Koreanischer Won  <br/> |
| 33  <br/> | LUF  <br/> | Luxemburgischer Franken  <br/> |
| 34  <br/> | MXN  <br/> | Mexikanischer Peso  <br/> |
| 35  <br/> | MYR  <br/> | Malaysischer Ringgit  <br/> |
| 36  <br/> | NLG  <br/> | Niederländischer Gulden  <br/> |
| 37  <br/> | NOK  <br/> | Norwegische Krone  <br/> |
| 38  <br/> | NZD  <br/> | Neuseeländischer Dollar  <br/> |
| 39  <br/> | PHP  <br/> | Philippinischer Peso  <br/> |
| 40  <br/> | PLZ (historisch. PLN verwenden.)  <br/> | Polnischer Zloty  <br/> |
| 41  <br/> | PTE  <br/> | Portugiesische Escudo  <br/> |
| 42  <br/> | ROL  <br/> | Rumänischer Leu  <br/> |
| 43  <br/> | RUR (historisch. RUB verwenden.)  <br/> | Russischer Rubel  <br/> |
| 44  <br/> | SEK  <br/> | Schwedische Kronen  <br/> |
| 45  <br/> | SGD  <br/> | Singapur-Dollar  <br/> |
| 46  <br/> | THB  <br/> | Thailändische Baht  <br/> |
| 47  <br/> | TWD  <br/> | Neuer Taiwan-Dollar  <br/> |
| 48  <br/> | XEU (historisch. Verwenden Sie EUR.)  <br/> | ECU (vor 1998)  <br/> |
| 49  <br/> | YUN (historisch. Verwenden Sie YUM.)  <br/> | Jugoslawischer Dinar  <br/> |
| 50  <br/> | ZAR  <br/> | Südafrikanischer Rand  <br/> |
| 51-55  <br/> | Reserved  <br/> |
| 56  <br/> | ARS  <br/> | Argentinischer Peso  <br/> |
| 57  <br/> | BMD  <br/> | Bermudian Dollar  <br/> |
| 58  <br/> | BOB  <br/> | Bolivianischen Boliviao  <br/> |
| 59  <br/> | BRR (historisch. Verwenden Sie BRL.)  <br/> | Brasilianische Cruziero Real  <br/> |
| 60  <br/> | BSD  <br/> | Bahamanian Dollar  <br/> |
| 61  <br/> | CLP  <br/> | Chilenischer Peso  <br/> |
| 62  <br/> | COP  <br/> | Kolumbianischer Peso  <br/> |
| 63  <br/> | CRC  <br/> | Costa Rican Colon  <br/> |
| 64  <br/> | CZK  <br/> | Tschechische Krone  <br/> |
| 65  <br/> | DOP  <br/> | Dominikanischer Peso  <br/> |
| 66  <br/> | ECS  <br/> | Ecuadorianische Sucre  <br/> |
| 67  <br/> | EGP  <br/> | Ägyptisches Pfund  <br/> |
| 68  <br/> | HNL  <br/> | Honduras Lempira  <br/> |
| 69  <br/> | INR  <br/> | Indische Rupie  <br/> |
| 70  <br/> | JMD  <br/> | Jamaikanische Dollar  <br/> |
| 71  <br/> | JOD  <br/> | Jordanischen Dinar  <br/> |
| 72  <br/> | KWD  <br/> | Kuwaiti Dinar  <br/> |
| 73  <br/> | MOP  <br/> | Macau Pataca  <br/> |
| 74  <br/> | NIO  <br/> | Nicaragua Cordoba Oro  <br/> |
| 75  <br/> | PAB  <br/> | Panamaischer Balboa  <br/> |
| 76  <br/> | Stift  <br/> | Peruanisches Nuevo Sol  <br/> |
| 77  <br/> | PKR  <br/> | Pakistanische Rupie  <br/> |
| 78  <br/> | PYG  <br/> | Paraguay Guarani  <br/> |
| 79  <br/> | SAR  <br/> | Saudi Riyal  <br/> |
| 80  <br/> | SITZEN  <br/> | Slowenischer Anwart  <br/> |
| 81  <br/> | SKK  <br/> | Slowakische Krone  <br/> |
| 82  <br/> | SVC  <br/> | El Salvador Doppelpunkt  <br/> |
| 83  <br/> | VERSUCHEN  <br/> | Neue türkische Lira  <br/> |
| 84  <br/> | TTD  <br/> | Trinidad und Tobago-Dollar  <br/> |
| 85  <br/> | UYU  <br/> | Uruguayisch  <br/> |
| 86  <br/> | VEB  <br/> | Venezolanischer Bolivar  <br/> |
| 87  <br/> | VND  <br/> | Vietnamesisch Dong  <br/> |
| 88  <br/> | BRL  <br/> | Brasilianisches Real  <br/> |
| 89  <br/> | PLN  <br/> | Polnischer Zloty  <br/> |
| 90  <br/> | REIBEN  <br/> | Russischer Rubel  <br/> |
| 91  <br/> | YUM  <br/> | Jugoslawischer Dinar  <br/> |
| 92  <br/> | BYB (historisch. Verwenden Sie BYR.)  <br/> | Weißrussischer Rubel  <br/> |
| 93  <br/> | UAH  <br/> | Ukrainische Griwna  <br/> |
| 94  <br/> | AFA  <br/> | Afghani (hinzugefügt in Visio 2002)  <br/> |
| 95  <br/> | ALLE  <br/> | Lek (hinzugefügt in Visio 2002)  <br/> |
| 96  <br/> | DZD  <br/> | Algerischer Dinar (hinzugefügt in Visio 2002)  <br/> |
| 97  <br/> | ADP  <br/> | Andorran Peseten (hinzugefügt in Visio 2002)  <br/> |
| 98  <br/> | AOA  <br/> | Kwanza (hinzugefügt in Visio 2002)  <br/> |
| 99  <br/> | XCD  <br/> | East Caribbean Dollar (hinzugefügt in Visio 2002)  <br/> |
| 100  <br/> | AMD  <br/> | Armenischer Dram (hinzugefügt in Visio 2002)  <br/> |
| 101  <br/> | AWG  <br/> | Aruban-Gulden (hinzugefügt in Visio 2002)  <br/> |
| 102  <br/> | AZM  <br/> | Aserbaidschanischen Manat (hinzugefügt in Visio 2002)  <br/> |
| 103  <br/> | BHD  <br/> | Bahraini Dinar (hinzugefügt in Visio 2002)  <br/> |
| 104  <br/> | BDT  <br/> | Taka (hinzugefügt in Visio 2002)  <br/> |
| 105  <br/> | BBD  <br/> | Barbados-Dollar (hinzugefügt in Visio 2002)  <br/> |
| 106  <br/> | BYR  <br/> | WeißRussischer Rubel (hinzugefügt in Visio 2002)  <br/> |
| 107  <br/> | BZD  <br/> | Belize-Dollar (hinzugefügt in Visio 2002)  <br/> |
| 108  <br/> | XOF  <br/> | CFA-Franc-BCEAO (hinzugefügt in Visio 2002)  <br/> |
| 109  <br/> | BTN  <br/> | Ngultrum (hinzugefügt in Visio 2002)  <br/> |
| 110  <br/> | BAM  <br/> | Konvertierbare Markierungen (hinzugefügt in Visio 2002)  <br/> |
| 111  <br/> | BWP  <br/> | Pula (hinzugefügt in Visio 2002)  <br/> |
| 112  <br/> | BND  <br/> | Brunei-Dollar (hinzugefügt in Visio 2002)  <br/> |
| 113  <br/> | BGL (historisch. Verwenden Sie BGN.)  <br/> | Lev  <br/> |
| 114  <br/> | BGN  <br/> | Bulgarischer Lev (hinzugefügt in Visio 2002)  <br/> |
| 115  <br/> | BIF  <br/> | Burundi Franken (hinzugefügt in Visio 2002)  <br/> |
| 116  <br/> | KHR  <br/> | Riel (hinzugefügt in Visio 2002)  <br/> |
| 117  <br/> | XAF  <br/> | CFA-Franc-BEAC (hinzugefügt in Visio 2002)  <br/> |
| 118  <br/> | CVE  <br/> | Kap Verde Escudo (hinzugefügt in Visio 2002)  <br/> |
| 119  <br/> | KYD  <br/> | Kaimaninseln-Dollar (hinzugefügt in Visio 2002)  <br/> |
| 120  <br/> | KMF  <br/> | "Moro Franc" (hinzugefügt in Visio 2002)  <br/> |
| 121  <br/> | CDF  <br/> | Franc-congolais (hinzugefügt in Visio 2002)  <br/> |
| 122  <br/> | HRK  <br/> | Kroatische Kuna (hinzugefügt in Visio 2002)  <br/> |
| 123  <br/> | Tasse  <br/> | Kubanischer Peso (hinzugefügt in Visio 2002)  <br/> |
| 124  <br/> | CYP  <br/> | Zypern-Pfund (hinzugefügt in Visio 2002)  <br/> |
| 125  <br/> | DJF  <br/> | Dschibuti-Franc (hinzugefügt in Visio 2002)  <br/> |
| 126  <br/> | TPE  <br/> | Timor Escudo (hinzugefügt in Visio 2002)  <br/> |
| 127  <br/> | ERN  <br/> | Nakfa (hinzugefügt in Visio 2002)  <br/> |
| 128  <br/> | EEK  <br/> | Krone (hinzugefügt in Visio 2002)  <br/> |
| 129  <br/> | ETB  <br/> | Äthiopisches Birr (hinzugefügt in Visio 2002)  <br/> |
| 130  <br/> | FKP  <br/> | Falklandinseln (Islas Malvinas) Pound (hinzugefügt in Visio 2002)  <br/> |
| 131  <br/> | FJD  <br/> | Fidschi-Dollar (hinzugefügt in Visio 2002)  <br/> |
| 132  <br/> | XPF  <br/> | CFP Franc (hinzugefügt in Visio 2002)  <br/> |
| 133  <br/> | GMD  <br/> | Dalasi (hinzugefügt in Visio 2002)  <br/> |
| 134  <br/> | GEL  <br/> | Lari (hinzugefügt in Visio 2002)  <br/> |
| 135  <br/> | GHC  <br/> | Cedi (hinzugefügt in Visio 2002)  <br/> |
| 136  <br/> | GIP  <br/> | Gibraltar-Pfund (hinzugefügt in Visio 2002)  <br/> |
| 137  <br/> | GTQ  <br/> | Quetzal (hinzugefügt in Visio 2002)  <br/> |
| 138  <br/> | GNF  <br/> | Guinea Franc (hinzugefügt in Visio 2002)  <br/> |
| 139  <br/> | GWP  <br/> | Guinea-Bissau-Peso (hinzugefügt in Visio 2002)  <br/> |
| 140  <br/> | GYD  <br/> | Guyana-Dollar (hinzugefügt in Visio 2002)  <br/> |
| 141  <br/> | HTG  <br/> | Kürbisse (hinzugefügt in Visio 2002)  <br/> |
| 142  <br/> | ISK  <br/> | Isländische Krone (hinzugefügt in Visio 2002)  <br/> |
| 143  <br/> | IKV  <br/> | Iranisches Rial (hinzugefügt in Visio 2002)  <br/> |
| 144  <br/> | IQD  <br/> | Irakischer Dinar (hinzugefügt in Visio 2002)  <br/> |
| 145  <br/> | KZT  <br/> | Tenge (hinzugefügt in Visio 2002)  <br/> |
| 146  <br/> | KES  <br/> | Kenianische Schilling (hinzugefügt in Visio 2002)  <br/> |
| 147  <br/> | KPW  <br/> | Nordkoreanischer Won (hinzugefügt in Visio 2002)  <br/> |
| 148  <br/> | KG  <br/> | SOM (hinzugefügt in Visio 2002)  <br/> |
| 149  <br/> | LAK  <br/> | Kip (hinzugefügt in Visio 2002)  <br/> |
| 150  <br/> | LVL (historisch. Verwenden Sie EUR.)  <br/> | Lettischer Lats (hinzugefügt in Visio 2002)  <br/> |
| 151  <br/> | LBP  <br/> | Libanesisches Pfund (hinzugefügt in Visio 2002)  <br/> |
| 152  <br/> | LSL  <br/> | Loti (hinzugefügt in Visio 2002)  <br/> |
| 153  <br/> | LRD  <br/> | Liberianische Dollar (hinzugefügt in Visio 2002)  <br/> |
| 154  <br/> | LYD  <br/> | Libyscher Dinar (hinzugefügt in Visio 2002)  <br/> |
| 155  <br/> | LTL  <br/> | Litauische Litus (hinzugefügt in Visio 2002)  <br/> |
| 156  <br/> | MKD  <br/> | Denar (hinzugefügt in Visio 2002)  <br/> |
| 157  <br/> | MGF (historisch. Verwenden Sie MGA.)  <br/> | Madagaskar-Franken (hinzugefügt in Visio 2002)  <br/> |
| 158  <br/> | MWK  <br/> | Malawi Kwacha (hinzugefügt in Visio 2002)  <br/> |
| 159  <br/> | MVR  <br/> | Rufiyaa (hinzugefügt in Visio 2002)  <br/> |
| 160  <br/> | MTL  <br/> | Maltesische Lira (hinzugefügt in Visio 2002)  <br/> |
| 161  <br/> | MRO  <br/> | Ouguiya (hinzugefügt in Visio 2002)  <br/> |
| 162  <br/> | MUR  <br/> | Mauritius-Rupie (hinzugefügt in Visio 2002)  <br/> |
| 163  <br/> | MDL  <br/> | Moldawischer Leu (hinzugefügt in Visio 2002)  <br/> |
| 164  <br/> | MNT  <br/> | Tugrik (hinzugefügt in Visio 2002)  <br/> |
| 165  <br/> | Ihrem  <br/> | Marokkanischer Dirham (hinzugefügt in Visio 2002)  <br/> |
| 166  <br/> | MZM  <br/> | Metical (hinzugefügt in Visio 2002)  <br/> |
| 167  <br/> | MMK  <br/> | Kyat (hinzugefügt in Visio 2002)  <br/> |
| 168  <br/> | NAD  <br/> | Namibia-Dollar (hinzugefügt in Visio 2002)  <br/> |
| 169  <br/> | NPR  <br/> | Nepalesische Rupie (hinzugefügt in Visio 2002)  <br/> |
| 170  <br/> | ANG  <br/> | Niederländische nl Gulden-Gulden (hinzugefügt in Visio 2002)  <br/> |
| 171  <br/> | NGN  <br/> | Naira (hinzugefügt in Visio 2002)  <br/> |
| 172  <br/> | OMR  <br/> | Rial Omani (hinzugefügt in Visio 2002)  <br/> |
| 173  <br/> | PGK  <br/> | (In Visio 2002 hinzugefügt)  <br/> |
| 174  <br/> | QAR  <br/> | Qatari Rial (hinzugefügt in Visio 2002)  <br/> |
| 175  <br/> | RWF  <br/> | Ruanda-Franc (hinzugefügt in Visio 2002)  <br/> |
| 176  <br/> | SHP  <br/> | St. Helena-Pfund (hinzugefügt in Visio 2002)  <br/> |
| 177  <br/> | WST  <br/> | Tala (hinzugefügt in Visio 2002)  <br/> |
| 178  <br/> | STD  <br/> | Dobra (hinzugefügt in Visio 2002)  <br/> |
| 179  <br/> | SCR  <br/> | Seychellen-Rupie (hinzugefügt in Visio 2002)  <br/> |
| 180  <br/> | SLL  <br/> | Leone (hinzugefügt in Visio 2002)  <br/> |
| 181  <br/> | SBD  <br/> | Salomonen-Dollar (hinzugefügt in Visio 2002)  <br/> |
| 182  <br/> | SOS  <br/> | Somalischer Schilling (hinzugefügt in Visio 2002)  <br/> |
| 183  <br/> | LKR  <br/> | Sri Lanka-Rupie (hinzugefügt in Visio 2002)  <br/> |
| 184  <br/> | SDD  <br/> | Sudanesische Dinar (hinzugefügt in Visio 2002)  <br/> |
| 185  <br/> | SRG  <br/> | Surinam-Gulden (hinzugefügt in Visio 2002)  <br/> |
| 186  <br/> | SZL  <br/> | Lilangeni (hinzugefügt in Visio 2002)  <br/> |
| 187  <br/> | SYP  <br/> | Syrisches Pfund (hinzugefügt in Visio 2002)  <br/> |
| 188  <br/> | TJR (historisch. Verwenden Sie TJS.)  <br/> | Tadschikistan Rubel  <br/> |
| 189  <br/> | TJS  <br/> | Tadschikistan Somoni (hinzugefügt in Visio 2002)  <br/> |
| 190  <br/> | TZS  <br/> | Tansanischen Schilling (hinzugefügt in Visio 2002)  <br/> |
| 191  <br/> | Nach oben  <br/> | PA ' anga (hinzugefügt in Visio 2002)  <br/> |
| 192  <br/> | TND  <br/> | Tunesischer Dinar (hinzugefügt in Visio 2002)  <br/> |
| 193  <br/> | TMM  <br/> | Manat (hinzugefügt in Visio 2002)  <br/> |
| 194  <br/> | UGX  <br/> | Uganda-Schilling (hinzugefügt in Visio 2002)  <br/> |
| 195  <br/> | AED  <br/> | UAE Dirham (hinzugefügt in Visio 2002)  <br/> |
| 196  <br/> | UZS  <br/> | Usbekistan Sum (hinzugefügt in Visio 2002)  <br/> |
| 197  <br/> | VUV  <br/> | Vatu (hinzugefügt in Visio 2002)  <br/> |
| 198  <br/> | YER  <br/> | Jemenitischen Rial (hinzugefügt in Visio 2002)  <br/> |
| 199  <br/> | ZMK  <br/> | Zambian Kwacha (hinzugefügt in Visio 2002)  <br/> |
| 200  <br/> | ZWD  <br/> | Simbabwe-Dollar (hinzugefügt in Visio 2002)  <br/> |
|201  <br/> |VEF  <br/> |Venezolanische Bolivar Fuente (hinzugefügt in Visio 2010)  <br/> |
|202  <br/> |MGA  <br/> |Madagaskar-Arie (hinzugefügt in Visio 2010)  <br/> |
|203  <br/> |RSD  <br/> |Serbischer Dinar (hinzugefügt in Visio 2010)  <br/> |
|204  <br/> |CSD (historisch. RSD verwenden.)  <br/> |Serbischer Dinar (hinzugefügt in Visio 2010)  <br/> |
   

