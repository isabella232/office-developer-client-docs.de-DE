---
title: Benannte Eigenschaften MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f0b1d080a1321ea9017126a2a996ceb593de2db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579586"
---
# <a name="mapi-named-properties"></a>Benannte Eigenschaften MAPI
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI bietet eine Möglichkeit zum Zuweisen von Namen zu Eigenschaften, zum Zuordnen dieser Namen zu eindeutigen Bezeichnern und zum Dauerhaften dieser Zuordnung. Durch beständige Zuordnung von Namen zu Bezeichnern wird sichergestellt, dass Eigenschaftsnamen sitzungsübergreifend gültig bleiben.
  
Um eine benannte Eigenschaft zu definieren, macht ein Client oder Dienstanbieter einen Namen und speichert ihn in einer [MAPINAMEID-Struktur.](mapinameid.md) Da Namen aus einem global eindeutigen 32-Bit-Bezeichner oder einer GUID und entweder einer Unicode-Zeichenfolge oder einem numerischen Wert bestehen, können Ersteller benannter Eigenschaften aussagekräftige Namen erstellen, ohne duplizieren zu müssen. Namen sind eindeutig und können ohne Berücksichtigung des Werts ihrer Bezeichner verwendet werden. 
  
Zur Unterstützung benannter Eigenschaften implementiert ein Dienstanbieter zwei Methoden – [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) –, um zwischen Namen und Bezeichnern zu übersetzen und seine [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps-Methoden](imapiprop-setprops.md) zum Abrufen und Ändern von Eigenschaften mit Bezeichnern im benannten Eigenschaftenbereich zuzulassen. Der Bereich für benannte Eigenschaftsbezeichner liegt zwischen 0x8000 und 0xFFFE. 
  
Jedes Objekt, das die **IMAPIProp-Schnittstelle** implementiert, kann benannte Eigenschaften unterstützen. Adressbuchanbieter, die das Kopieren von Einträgen von anderen Anbietern in ihre Container zulassen, und Nachrichtenspeicheranbieter, die zum Erstellen beliebiger Nachrichtentypen verwendet werden können, sind erforderlich, um diese Unterstützung zu bieten. Es ist eine Option für alle anderen Dienstanbieter. Anbieter, die keine benannten Eigenschaften unterstützen, geben MAPI_E_NO_SUPPORT aus den Methoden **GetIDsFromNames** und **GetNamesFromIDs** zurück und verweigern das Festlegen von Eigenschaften mit Bezeichnern von 0x8000 oder höher, wodurch MAPI_E_UNEXPECTED im **SPropProblemarray** zurückgegeben wird.
  
Das Erstellen von Namen für Eigenschaften ist eine Möglichkeit für Clients, neue Eigenschaften für vorhandene oder benutzerdefinierte Nachrichtenklassen zu definieren. Dienstanbieter können benannte Eigenschaften verwenden, um eindeutige Features ihrer Messagingsysteme verfügbar zu machen. Eine weitere Verwendung für benannte Eigenschaften besteht darin, eine alternative Möglichkeit zum Verweisen auf Eigenschaften mit Bezeichnern unter 0x8000 bereitzustellen. 
  
Beispielsweise könnte ein Client Code ähnlich dem folgenden Code verwenden, um die Namen für alle benannten Eigenschaften eines Objekts abzurufen:
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

Um alle Namen aus dem PS_PUBLIC_STRINGS Eigenschaftensatz anzufordern, würde ein Client den NULL-Wert im Eigenschaftensatzparameter wie folgt in PS_PUBLIC_STRINGS ersetzen: 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

