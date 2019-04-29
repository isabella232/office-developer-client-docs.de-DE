---
title: Benannte Eigenschaften MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435047"
---
# <a name="mapi-named-properties"></a>Benannte Eigenschaften MAPI
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI bietet eine Möglichkeit zum Zuweisen von Namen zu Eigenschaften, um diese Namen eindeutigen Bezeichnern zuzuordnen und diese Zuordnung persistent zu machen. Persistent Name to Identifier Mapping stellt sicher, dass Eigenschaftsnamen in allen Sitzungen gültig bleiben.
  
Zum Definieren einer benannten Eigenschaft erstellt ein Client oder Dienstanbieter einen Namen und speichert ihn in einer [MAPINAMEID](mapinameid.md) -Struktur. Da Namen aus einem global eindeutigen 32-Bit-Bezeichner oder einer GUID und entweder einer Unicode-Zeichenfolge oder einem numerischen Wert bestehen, können Ersteller benannter Eigenschaften aussagekräftige Namen erstellen, ohne dass eine Duplizierung vorliegt. Namen sind eindeutig und können unabhängig vom Wert ihrer Bezeichner verwendet werden. 
  
Zur Unterstützung benannter Eigenschaften implementiert ein Dienstanbieter zwei Methoden – [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) –, um zwischen Namen und Bezeichnern zu übersetzen und ihre IMAPIProp zu ermöglichen [:: GetProps](imapiprop-getprops.md) [ IMAPIProp::](imapiprop-setprops.md) SetProps-Methoden zum Abrufen und Ändern von Eigenschaften mit Bezeichnern im benannten Eigenschaftenbereich. Der Range für benannte Eigenschaftsbezeichner liegt zwischen 0X8000 und 0xFFFE. 
  
Jedes Objekt, das die **IMAPIProp** -Schnittstelle implementiert, kann benannte Eigenschaften unterstützen. Adressbuchanbieter, die das Kopieren von Einträgen anderer Anbieter in Ihre Container und Nachrichtenspeicher Anbieter zulassen, die zum Erstellen beliebiger Nachrichtentypen verwendet werden können, sind erforderlich, um diese Unterstützung bereitzustellen. Dies ist eine Option für alle anderen Dienstanbieter. Anbieter, die benannte Eigenschaften nicht unterstützen, geben MAPI_E_NO_SUPPORT aus der **GetIDsFromNames** -und der **GetNamesFromIDs** -Methode zurück und lehnen das Festlegen von Eigenschaften mit Bezeichnern von 0X8000 oder höher ab und geben MAPI_E_UNEXPECTED in der ** SPropProblemarray**.
  
Das Erstellen von Namen für Eigenschaften ist eine Möglichkeit für Clients, neue Eigenschaften für vorhandene oder benutzerdefinierte Nachrichtenklassen zu definieren. Dienstanbieter können benannte Eigenschaften verwenden, um eindeutige Features Ihrer Messagingsysteme anzuzeigen. Eine weitere Verwendung für benannte Eigenschaften besteht darin, eine alternative Möglichkeit zum Verweisen auf Eigenschaften mit Bezeichnern unter 0X8000 bereitzustellen. 
  
Ein Client könnte beispielsweise Code verwenden, der dem folgenden Code ähnelt, um die Namen für alle benannten Eigenschaften eines Objekts abzurufen:
  
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

Um alle Namen aus dem PS_PUBLIC_STRINGS-Eigenschaftensatz anzufordern, würde ein Client den NULL-Wert im Eigenschaftensatz-Parameter wie folgt in PS_PUBLIC_STRINGS ersetzen: 
  
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

