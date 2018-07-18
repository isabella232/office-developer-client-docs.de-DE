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
description: Um eine Zahl als Währung formatieren möchten, können Sie die CY-Funktion verwenden und eine optionale Konstante, um anzugeben, welche Land/Region, die zu verwendende Währung übergeben. Die Währungskonstanten können angegeben werden, als die ID-Nummer, die ein Land/Region entspricht, oder als eine Zeichenfolge (in Anführungszeichen eingeschlossen), die Abkürzung dreistelligen ISO 4217 entspricht.
ms.openlocfilehash: ce27cbcb03b4c41cce3cf08fbcd234678fcdc773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796374"
---
# <a name="about-currency-constants"></a>Informationen zu Währungskonstanten

Um eine Zahl als Währung formatieren möchten, können Sie die CY-Funktion verwenden und eine optionale Konstante, um anzugeben, welche Land/Region, die zu verwendende Währung übergeben. Die Währungskonstanten können angegeben werden, als die ID-Nummer, die ein Land/Region entspricht, oder als eine Zeichenfolge (in Anführungszeichen eingeschlossen), die Abkürzung dreistelligen ISO 4217 entspricht.
  
Wenn Sie die Währungssymbole für nicht lokalen Währungen anzeigen, und das System nicht das Symbol für einen bestimmten Währung weiß, wird das Euro-Symbol ($) angezeigt.
  
## <a name="ids-and-abbreviations"></a>-IDs und Abkürzungen

|**ID**|**Abbreviation**|**Currency**|
|:-----|:-----|:-----|
| 0  <br/> | SYS  <br/> | Systemeinstellungen verwendet  <br/> |
| 1  <br/> | XXX  <br/> | Formate als Zahl  <br/> |
| 2 - 9  <br/> | Reserviert  <br/> |
| 10  <br/> | EUR  <br/> | Euro  <br/> |
| 11  <br/> | US-DOLLAR  <br/> | US-dollar  <br/> |
| 12  <br/> | ATS  <br/> | Österreichische Schilling  <br/> |
| 13  <br/> | AUD  <br/> | Australien Dollar  <br/> |
| 14  <br/> | BEF  <br/> | Belgische Franc  <br/> |
| 15  <br/> | CAD  <br/> | Kanadische Dollar  <br/> |
| 16  <br/> | CHF  <br/> | Swiss Franc  <br/> |
| 17  <br/> | CNY  <br/> | Chinesischer Renminbi Yuan  <br/> |
| 18  <br/> | DEM  <br/> | Deutsche Mark  <br/> |
| 19  <br/> | DKK  <br/> | Dänische Kronen  <br/> |
| 20  <br/> | ESP  <br/> | Spanische Peseten  <br/> |
| 21  <br/> | FIM  <br/> | Finnische Mark  <br/> |
| 22  <br/> | FRF  <br/> | Französische Franc  <br/> |
| 23  <br/> | GBP  <br/> | Britisches Pfund Sterling  <br/> |
| 24  <br/> | GRD  <br/> | Griechische Drachmen  <br/> |
| 25  <br/> | HKD  <br/> | Hongkong Kong spezielle Administrative Region (SAR) Euro  <br/> |
| 26  <br/> | HUF  <br/> | Ungarisch FT  <br/> |
| 27  <br/> | IDR  <br/> | Indonesisch Rupiah  <br/> |
| 28  <br/> | IEP  <br/> | Irisches Pfund  <br/> |
| 29  <br/> | ILS  <br/> | Israel Schekel  <br/> |
| 30  <br/> | ITL  <br/> | Italienische Lire  <br/> |
| 31  <br/> | JPY  <br/> | Japanische Yen  <br/> |
| 32  <br/> | KRW  <br/> | Koreanisch gewonnen  <br/> |
| 33  <br/> | LUF  <br/> | Luxemburgische Franc  <br/> |
| 34  <br/> | MXN  <br/> | Mexikanisches Peso  <br/> |
| 35  <br/> | MYR  <br/> | Malaysia Ringgit  <br/> |
| 36  <br/> | NLG  <br/> | Niederländische Gulden  <br/> |
| 37  <br/> | NOK  <br/> | Norwegisch Kronen  <br/> |
| 38  <br/> | NZD  <br/> | Neuseeland Dollar  <br/> |
| 39  <br/> | PHP  <br/> | Philippinen Peso  <br/> |
| 40  <br/> | PLZ (Archiv. Verwenden Sie PLN.)  <br/> | Polnisch Zloty  <br/> |
| 41  <br/> | PTE  <br/> | Portugiesische Escudos  <br/> |
| 42  <br/> | ROL  <br/> | Rumänisch Leu  <br/> |
| 43  <br/> | RUR (Archiv. Verwenden Sie Problem).  <br/> | Russische Rubel  <br/> |
| 44  <br/> | SEK  <br/> | Schwedische Kronen  <br/> |
| 45  <br/> | SGD  <br/> | Singapur Dollar  <br/> |
| 46  <br/> | THB  <br/> | Thailändische Baht  <br/> |
| 47  <br/> | TWD  <br/> | Neue Taiwandollar  <br/> |
| 48  <br/> | XEU (Archiv. Verwenden Sie EUR)  <br/> | ECU (vor 1998)  <br/> |
| 49  <br/> | YUN (Archiv. Verwenden Sie YUM.)  <br/> | Jugoslawischer Dinar  <br/> |
| 50  <br/> | ZAR  <br/> | Südafrika Rand  <br/> |
| 51 - 55  <br/> | Reserviert  <br/> |
| 56  <br/> | ARS  <br/> | Argentinien Peso  <br/> |
| 57  <br/> | BMD  <br/> | Bermudian Dollar  <br/> |
| 58  <br/> | BOB  <br/> | Bolivien Boliviano  <br/> |
| 59  <br/> | BRR (Archiv. Verwenden Sie BRL.)  <br/> | Brasilianischer Cruziero Real  <br/> |
| 60  <br/> | BSD  <br/> | Bahamanian Dollar  <br/> |
| 61  <br/> | CLP  <br/> | Chile Peso  <br/> |
| 62  <br/> | KOPIEREN  <br/> | Kolumbien Peso  <br/> |
| 63  <br/> | CRC  <br/> | Costa Rica Doppelpunkt  <br/> |
| 64  <br/> | CZK  <br/> | Tschechische Kronen  <br/> |
| 65  <br/> | DOP  <br/> | Dominikanische Peso  <br/> |
| 66  <br/> | ECS  <br/> | Ecuadorianischem Sucre  <br/> |
| 67  <br/> | EGP  <br/> | Ägypten Pfund  <br/> |
| 68  <br/> | HNL  <br/> | Honduras Lempira  <br/> |
| 69  <br/> | INR  <br/> | Indischer Rupie  <br/> |
| 70  <br/> | JMD  <br/> | Jamaika-Dollar  <br/> |
| 71  <br/> | JOD  <br/> | Jordanischer Dinar  <br/> |
| 72  <br/> | KWD  <br/> | Kuwait Dinar  <br/> |
| 73  <br/> | WISCHEN  <br/> | In Macau Pataca  <br/> |
| 74  <br/> | NIO  <br/> | Nicaragua Cordoba Oro  <br/> |
| 75  <br/> | PAB  <br/> | Panama Balboa  <br/> |
| 76  <br/> | STIFT  <br/> | Peruanischer Sol  <br/> |
| 77  <br/> | PKR  <br/> | Pakistan Rupie  <br/> |
| 78  <br/> | PYG  <br/> | Paraguay Guarani  <br/> |
| 79  <br/> | SAR  <br/> | Saudi Rial  <br/> |
| 80  <br/> | SIT  <br/> | Slowenisch Tolar  <br/> |
| 81  <br/> | SKK  <br/> | Slowakische Kronen  <br/> |
| 82  <br/> | SVC  <br/> | El Salvador Doppelpunkt  <br/> |
| 83  <br/> | VERSUCHEN SIE ES  <br/> | Neue Türkisch Lire  <br/> |
| 84  <br/> | TTD  <br/> | Trinidad und Tobago Dollar  <br/> |
| 85  <br/> | UYU  <br/> | Uruguay Peso Uruguayo  <br/> |
| 86  <br/> | VEB  <br/> | Venezuela Bolivar  <br/> |
| 87  <br/> | VND  <br/> | Vietnamesisch Dong  <br/> |
| 88  <br/> | BRL  <br/> | Portugiesisch (Brasilien) reelle Zahl  <br/> |
| 89  <br/> | PLN  <br/> | Polnisch Zloty  <br/> |
| 90  <br/> | PROBLEM  <br/> | Russische Rubel  <br/> |
| 91  <br/> | YUM  <br/> | Jugoslawischer Dinar  <br/> |
| 92  <br/> | BYB (Archiv. Verwenden Sie BYR.)  <br/> | Belarussisch Rubel  <br/> |
| 93  <br/> | UAH  <br/> | Ukrainisch bei Freigabe  <br/> |
| 94  <br/> | AFA  <br/> | Afghani (in Visio 2002 hinzugefügt)  <br/> |
| 95  <br/> | ALL  <br/> | Lek (in Visio 2002 hinzugefügt)  <br/> |
| 96  <br/> | DZD  <br/> | Algerien Dinar (in Visio 2002 hinzugefügt)  <br/> |
| 97  <br/> | ADP  <br/> | Andorranischer Peseten (in Visio 2002 hinzugefügt)  <br/> |
| 98  <br/> | AOA  <br/> | Kwanza (in Visio 2002 hinzugefügt)  <br/> |
| 99  <br/> | XCD  <br/> | East Karibik Dollar (in Visio 2002 hinzugefügt)  <br/> |
| 100  <br/> | AMD  <br/> | Armenisch Dram (in Visio 2002 hinzugefügt)  <br/> |
| 101  <br/> | AWG  <br/> | Aruban Gulden (in Visio 2002 hinzugefügt)  <br/> |
| 102  <br/> | AZM  <br/> | Aserbeijan Manat (in Visio 2002 hinzugefügt)  <br/> |
| 103  <br/> | BHD  <br/> | Bahrain Dinar (in Visio 2002 hinzugefügt)  <br/> |
| 104  <br/> | BDT  <br/> | Taka (in Visio 2002 hinzugefügt)  <br/> |
| 105  <br/> | BBD  <br/> | Barbados-Dollar (in Visio 2002 hinzugefügt)  <br/> |
| 106  <br/> | BYR  <br/> | Belarussisch Rubel (in Visio 2002 hinzugefügt)  <br/> |
| 107  <br/> | BZD  <br/> | Belize-Dollar (in Visio 2002 hinzugefügt)  <br/> |
| 108  <br/> | XOF  <br/> | CFA Franc BCEAO (in Visio 2002 hinzugefügt)  <br/> |
| 109  <br/> | BTN  <br/> | Ngultrum (in Visio 2002 hinzugefügt)  <br/> |
| 110  <br/> | BAM  <br/> | Konvertiert markiert (in Visio 2002 hinzugefügt)  <br/> |
| 111  <br/> | BWP  <br/> | Pula (in Visio 2002 hinzugefügt)  <br/> |
| 112  <br/> | BERAND  <br/> | Brunei-Dollar (in Visio 2002 hinzugefügt)  <br/> |
| 113  <br/> | BGL (Archiv. Verwenden Sie BGN.)  <br/> | Lev  <br/> |
| 114  <br/> | BGN  <br/> | Lew (in Visio 2002 hinzugefügt)  <br/> |
| 115  <br/> | BIF  <br/> | Burundi Franc (in Visio 2002 hinzugefügt)  <br/> |
| 116  <br/> | KHR  <br/> | Riel (in Visio 2002 hinzugefügt)  <br/> |
| 117  <br/> | XAF  <br/> | CFA Franc BEAC (in Visio 2002 hinzugefügt)  <br/> |
| 118  <br/> | CVE  <br/> | Kap Verde Escudos (in Visio 2002 hinzugefügt)  <br/> |
| 119  <br/> | DOLLARR  <br/> | Kaimaninseln-Dollar (in Visio 2002 hinzugefügt)  <br/> |
| 120  <br/> | KMF  <br/> | Komoren Franc (in Visio 2002 hinzugefügt)  <br/> |
| 121  <br/> | CDF  <br/> | Kongo-Franc (in Visio 2002 hinzugefügt)  <br/> |
| 122  <br/> | HRK  <br/> | Kroatisch Kuna (in Visio 2002 hinzugefügt)  <br/> |
| 123  <br/> | TASSE  <br/> | Kubanischer Peso (in Visio 2002 hinzugefügt)  <br/> |
| 124  <br/> | CYP  <br/> | Zypern Pfund (in Visio 2002 hinzugefügt)  <br/> |
| 125  <br/> | DJF  <br/> | Dschibuti Franc (in Visio 2002 hinzugefügt)  <br/> |
| 126  <br/> | TPE  <br/> | Timor Escudos (in Visio 2002 hinzugefügt)  <br/> |
| 127  <br/> | PENNSYLVANIAS  <br/> | Nakfa (in Visio 2002 hinzugefügt)  <br/> |
| 128  <br/> | EEK  <br/> | Kroon (in Visio 2002 hinzugefügt)  <br/> |
| 129  <br/> | ETB  <br/> | Äthiopisch Birr (in Visio 2002 hinzugefügt)  <br/> |
| 130  <br/> | FKP  <br/> | Falklandinseln (Islas Malvinas) Pfund (in Visio 2002 hinzugefügt)  <br/> |
| 131  <br/> | FJD  <br/> | Fidschi-Dollar (in Visio 2002 hinzugefügt)  <br/> |
| 132  <br/> | XPF  <br/> | GFP Franc (in Visio 2002 hinzugefügt)  <br/> |
| 133  <br/> | GMD  <br/> | Dalasi (in Visio 2002 hinzugefügt)  <br/> |
| 134  <br/> | GEL  <br/> | Lari (in Visio 2002 hinzugefügt)  <br/> |
| 135  <br/> | GHC  <br/> | Cedi (in Visio 2002 hinzugefügt)  <br/> |
| 136  <br/> | GIP  <br/> | Gibraltar Pfund (in Visio 2002 hinzugefügt)  <br/> |
| 137  <br/> | GTQ  <br/> | Quetzal (in Visio 2002 hinzugefügt)  <br/> |
| 138  <br/> | GNF  <br/> | Guinea Franc (in Visio 2002 hinzugefügt)  <br/> |
| 139  <br/> | GWP  <br/> | Guinea-Bissau Peso (in Visio 2002 hinzugefügt)  <br/> |
| 140  <br/> | GYD  <br/> | Guyana-Dollar (in Visio 2002 hinzugefügt)  <br/> |
| 141  <br/> | HEIZ.  <br/> | Gourde (in Visio 2002 hinzugefügt)  <br/> |
| 142  <br/> | ISK  <br/> | Island Kronen (in Visio 2002 hinzugefügt)  <br/> |
| 143  <br/> | IRR  <br/> | Iran Rial (in Visio 2002 hinzugefügt)  <br/> |
| 144  <br/> | IQD  <br/> | Irak Dinar (in Visio 2002 hinzugefügt)  <br/> |
| 145  <br/> | KZT  <br/> | Tenge (in Visio 2002 hinzugefügt)  <br/> |
| 146  <br/> | KES  <br/> | Kenia-Schilling (in Visio 2002 hinzugefügt)  <br/> |
| 147  <br/> | KPW  <br/> | North Koreanisch gewonnen (in Visio 2002 hinzugefügt)  <br/> |
| 148  <br/> | KG  <br/> | SOM (in Visio 2002 hinzugefügt)  <br/> |
| 149  <br/> | LAK  <br/> | Kip (in Visio 2002 hinzugefügt)  <br/> |
| 150  <br/> | Einstufige (Archiv. Verwenden Sie EUR)  <br/> | Lettisch Lats (in Visio 2002 hinzugefügt)  <br/> |
| 151  <br/> | LBP  <br/> | Libanon Pfund (in Visio 2002 hinzugefügt)  <br/> |
| 152  <br/> | LSL  <br/> | Loti (in Visio 2002 hinzugefügt)  <br/> |
| 153  <br/> | LRD  <br/> | Liberianischer Dollar (in Visio 2002 hinzugefügt)  <br/> |
| 154  <br/> | LYD  <br/> | Libyen Dinar (in Visio 2002 hinzugefügt)  <br/> |
| 155  <br/> | LTL  <br/> | Litauisch Litus (in Visio 2002 hinzugefügt)  <br/> |
| 156  <br/> | MKD  <br/> | Denar (in Visio 2002 hinzugefügt)  <br/> |
| 157  <br/> | MGF (Archiv. Verwenden Sie MGA.)  <br/> | Madagaskar Franc (in Visio 2002 hinzugefügt)  <br/> |
| 158  <br/> | MWK  <br/> | Malawi Kwacha (in Visio 2002 hinzugefügt)  <br/> |
| 159  <br/> | MVR  <br/> | Rufiyaa (in Visio 2002 hinzugefügt)  <br/> |
| 160  <br/> | MTL  <br/> | Maltesisch Lire (in Visio 2002 hinzugefügt)  <br/> |
| 161  <br/> | MRO  <br/> | Ouguiya (in Visio 2002 hinzugefügt)  <br/> |
| 162  <br/> | MUR  <br/> | Mauritius Rupie (in Visio 2002 hinzugefügt)  <br/> |
| 163  <br/> | MDL  <br/> | Moldau-Leu (in Visio 2002 hinzugefügt)  <br/> |
| 164  <br/> | MNT  <br/> | Tugrik (in Visio 2002 hinzugefügt)  <br/> |
| 165  <br/> | SCHÖPFEN  <br/> | Marokko Dirham (in Visio 2002 hinzugefügt)  <br/> |
| 166  <br/> | MZM  <br/> | Metical (in Visio 2002 hinzugefügt)  <br/> |
| 167  <br/> | MMK  <br/> | Kyat (in Visio 2002 hinzugefügt)  <br/> |
| 168  <br/> | NAD  <br/> | Namibia-Dollar (in Visio 2002 hinzugefügt)  <br/> |
| 169  <br/> | NPR  <br/> | Nepalesische Rupie (in Visio 2002 hinzugefügt)  <br/> |
| 170  <br/> | ANG  <br/> | Niederlande NL Gulden (in Visio 2002 hinzugefügt)  <br/> |
| 171  <br/> | NGN  <br/> | Naira (in Visio 2002 hinzugefügt)  <br/> |
| 172  <br/> | OMR  <br/> | Rial Oman (in Visio 2002 hinzugefügt)  <br/> |
| 173  <br/> | PGK  <br/> | Kina (in Visio 2002 hinzugefügt)  <br/> |
| 174  <br/> | QAR  <br/> | Katar-Rial (in Visio 2002 hinzugefügt)  <br/> |
| 175  <br/> | RWF  <br/> | Ruanda Franc (in Visio 2002 hinzugefügt)  <br/> |
| 176  <br/> | SHP  <br/> | Saint Helena Pfund (in Visio 2002 hinzugefügt)  <br/> |
| 177  <br/> | WST  <br/> | Tala (in Visio 2002 hinzugefügt)  <br/> |
| 178  <br/> | STD  <br/> | Dobra (in Visio 2002 hinzugefügt)  <br/> |
| 179  <br/> | SCR  <br/> | Seychellen Rupie (in Visio 2002 hinzugefügt)  <br/> |
| 180  <br/> | SSL ANGEFORDERT WIRD  <br/> | Leone (in Visio 2002 hinzugefügt)  <br/> |
| 181  <br/> | SBD  <br/> | Salomonen-Dollar (in Visio 2002 hinzugefügt)  <br/> |
| 182  <br/> | SOS  <br/> | Somali Schilling (in Visio 2002 hinzugefügt)  <br/> |
| 183  <br/> | LKR  <br/> | Bangladesch Rupie (in Visio 2002 hinzugefügt)  <br/> |
| 184  <br/> | SDD  <br/> | Sudanesischer Dinar (in Visio 2002 hinzugefügt)  <br/> |
| 185  <br/> | SRG  <br/> | Suriname Gulden (in Visio 2002 hinzugefügt)  <br/> |
| 186  <br/> | SZL  <br/> | Lilangeni (in Visio 2002 hinzugefügt)  <br/> |
| 187  <br/> | SYP  <br/> | Syrisch Pfund (in Visio 2002 hinzugefügt)  <br/> |
| 188  <br/> | TJR (Archiv. Verwenden Sie TJS.)  <br/> | Tadschikisch Rubel  <br/> |
| 189  <br/> | TJS  <br/> | Tadschikisch Somoni (in Visio 2002 hinzugefügt)  <br/> |
| 190  <br/> | TZS  <br/> | Tansanischer Schilling (in Visio 2002 hinzugefügt)  <br/> |
| 191  <br/> | Nach oben  <br/> | Pa'anga (in Visio 2002 hinzugefügt)  <br/> |
| 192  <br/> | TND  <br/> | Tunesien Dinar (in Visio 2002 hinzugefügt)  <br/> |
| 193  <br/> | TMM  <br/> | Manat (in Visio 2002 hinzugefügt)  <br/> |
| 194  <br/> | UGX  <br/> | Uganda-Schilling (in Visio 2002 hinzugefügt)  <br/> |
| 195  <br/> | AED  <br/> | Vereinigte Arabische Emirate Dirham (in Visio 2002 hinzugefügt)  <br/> |
| 196  <br/> | UZS  <br/> | Usbekistan Sum (in Visio 2002 hinzugefügt)  <br/> |
| 197  <br/> | VUV  <br/> | Vatu (in Visio 2002 hinzugefügt)  <br/> |
| 198  <br/> | PASSWORT  <br/> | Jemen-Rial (in Visio 2002 hinzugefügt)  <br/> |
| 199  <br/> | ZMK  <br/> | Sambischer Kwacha (in Visio 2002 hinzugefügt)  <br/> |
| 200  <br/> | ZWD  <br/> | Simbabwe-Dollar (in Visio 2002 hinzugefügt)  <br/> |
|201  <br/> |VEF  <br/> |Venezuela Bolivar Fuente (hinzugefügt in Visio 2010)  <br/> |
|202  <br/> |MGA  <br/> |Madagassischen Ariary (hinzugefügt in Visio 2010)  <br/> |
|203  <br/> |RSD  <br/> |Serbisch Dinar (hinzugefügt in Visio 2010)  <br/> |
|204  <br/> |CSD (Archiv. Verwenden Sie RSD.)  <br/> |Serbisch Dinar (hinzugefügt in Visio 2010)  <br/> |
   

