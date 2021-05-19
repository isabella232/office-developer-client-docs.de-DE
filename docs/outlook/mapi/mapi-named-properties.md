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
  
MAPI bietet eine Möglichkeit zum Zuweisen von Namen zu Eigenschaften, zum Zuordnen dieser Namen zu eindeutigen Bezeichnern und zum Dauerhaften dieser Zuordnung. Die Zuordnung von beständigen Namen zu Bezeichnern stellt sicher, dass Eigenschaftsnamen für alle Sitzungen gültig bleiben.
  
Um eine benannte Eigenschaft zu definieren, stellt ein Client oder Dienstanbieter einen Namen zusammen und speichert ihn in einer [MAPINAMEID-Struktur.](mapinameid.md) Da Namen aus einer 32-Bit-GUID oder einer eindeutigen 32-Bit-ID und einer Unicode-Zeichenzeichenfolge oder einem numerischen Wert besteht, können Ersteller benannter Eigenschaften aussagekräftige Namen erstellen, ohne sich vor Duplizierungen zu fürchten. Namen sind eindeutig und können unabhängig vom Wert ihrer Bezeichner verwendet werden. 
  
Zur Unterstützung benannter Eigenschaften implementiert ein Dienstanbieter zwei Methoden – [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) und [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) –, um zwischen Namen und Bezeichnern zu übersetzen und die [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps-Methoden](imapiprop-setprops.md) zum Abrufen und Ändern von Eigenschaften mit Bezeichnern im benannten Eigenschaftenbereich zu ermöglichen. Der Bereich für benannte Eigenschaftenbezeichner liegt zwischen 0x8000 und 0xFFFE. 
  
Jedes Objekt, das die **IMAPIProp-Schnittstelle** implementiert, kann benannte Eigenschaften unterstützen. Adressbuchanbieter, die das Kopieren von Einträgen von anderen Anbietern in ihre Container zulassen, und Nachrichtenspeicheranbieter, die zum Erstellen beliebiger Nachrichtentypen verwendet werden können, sind für diese Unterstützung erforderlich. Es ist eine Option für alle anderen Dienstanbieter. Anbieter, die benannte Eigenschaften nicht unterstützen, geben MAPI_E_NO_SUPPORT von den **Methoden GetIDsFromNames** und **GetNamesFromIDs** zurück und weigern sich, Eigenschaften mit Bezeichnern von 0x8000 oder höher zu setzen, und geben MAPI_E_UNEXPECTED im **SPropProblemarray** zurück.
  
Das Erstellen von Namen für Eigenschaften ist eine Möglichkeit für Clients, neue Eigenschaften für vorhandene oder benutzerdefinierte Nachrichtenklassen zu definieren. Dienstanbieter können benannte Eigenschaften verwenden, um eindeutige Features ihrer Messagingsysteme verfügbar zu machen. Eine weitere Verwendung für benannte Eigenschaften besteht in der Bereitstellung einer alternativen Möglichkeit zum Verweisen auf Eigenschaften mit Bezeichnern 0x8000. 
  
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

Um alle Namen aus dem eigenschaftensatz PS_PUBLIC_STRINGS an fordern, würde ein Client den NULL-Wert im Eigenschaftssatzparameter wie folgt PS_PUBLIC_STRINGS ersetzen: 
  
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

