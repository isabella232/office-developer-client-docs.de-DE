---
title: Benannte Eigenschaften MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e755c18ef3cc32f9a00169f19cf336eace447a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793025"
---
# <a name="mapi-named-properties"></a>Benannte Eigenschaften MAPI
 
**Betrifft**: Outlook 
  
MAPI bietet die Möglichkeit zum Zuweisen von Namen zu Eigenschaften, um Managementsystems eindeutige Bezeichner zuzuordnen, sowie für diese Zuordnung persistent. Beständigen Namen Bezeichner Zuordnung wird sichergestellt, dass Eigenschaftennamen in allen Sitzungen gültig.
  
Zum Definieren einer benannten Eigenschaft ein Client oder Dienstanbieter bildet einen Namen und speichert sie in einer [MAPINAMEID](mapinameid.md) Struktur. Da Namen von einen global eindeutigen Bezeichner der 32-Bit, oder die GUID und entweder ein Unicode-Zeichen Zeichenfolge oder eines numerischen Wert vorgenommen werden, können Ersteller von benannten Eigenschaften aussagekräftige Namen des Duplizierung Wiederholungsversuchs erstellen. Namen sind eindeutig, und sie können verwendet werden, ohne dabei den Wert der ihre-IDs zu berücksichtigen. 
  
Zur Unterstützung der benannter Eigenschaften auf ein Dienstanbieter implementiert zwei Methoden – [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) – übersetzen zwischen Namen und Bezeichner und seine [IMAPIProp::GetProps](imapiprop-getprops.md) [ ermöglichen IMAPIProp::SetProps](imapiprop-setprops.md) Methoden zum Abrufen und Ändern von Eigenschaften mit Bezeichnern im Bereich benannten Eigenschaft. Der Bereich für benannte Eigenschaftenbezeichner liegt zwischen 0 x 8000 und 0xFFFE. 
  
Jedes Objekt, das die **IMAPIProp** -Schnittstelle implementiert wird, kann benannte Eigenschaften unterstützt. Von adressbuchanbietern implementierte, die es ermöglichen, dass Einträge von anderen Anbietern in ihre Container und die Nachricht kopiert werden Anbieter speichern, die zum Erstellen von beliebigen Nachrichtentypen verwendet werden können sind erforderlich, um diese Unterstützung bereitzustellen. Es ist eine Option für alle anderen Dienstanbieter. Anbieter, die keine Unterstützung für benannte Eigenschaften MAPI_E_NO_SUPPORT aus den Methoden **GetIDsFromNames** und **GetNamesFromIDs** zurückzugeben und Eigenschaften mit IDs der 0 x 8000 oder höher, Rückgabe MAPI_E_UNEXPECTED festgelegt werden, in der **Verweigern SPropProblemarray**.
  
Erstellen von Namen für Eigenschaften ist eine Möglichkeit für Clients, um neue Eigenschaften für vorhandenen oder benutzerdefinierten Nachrichtenklassen definieren. Benannte Eigenschaften können Dienstanbieter um einzigartigen Merkmale von messaging-Systemen verfügbar zu machen. Geben Sie eine alternative Möglichkeit zum Verweisen auf Eigenschaften mit Bezeichnern unter 0 x 8000 ist eine andere Verwendung für benannte Eigenschaften. 
  
Beispielsweise konnte ein Client ähnlichen Code wie den folgenden Code verwenden, um die Namen aller benannten Eigenschaften eines Objekts abzurufen:
  
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

Um die Namen aller aus dem Eigenschaftensatz PS_PUBLIC_STRINGS anzufordern, würde ein Client NULL in der Property Set-Parameters, PS_PUBLIC_STRINGS wie folgt ersetzen: 
  
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

- [�bersicht �ber die MAPI-Eigenschaft](mapi-property-overview.md)

