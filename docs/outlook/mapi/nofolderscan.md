---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3416bc50e4628df2be09f9fe1a22d19530bcdff8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578052"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob Microsoft Office Outlook-Ordner Kontakte in einem Speicher gescannt werden sollen.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Eingeblendet auf:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt  <br/> |
|Erstellt:  <br/> |Speicheranbieter  <br/> |
|Durch zugegriffen:  <br/> |Outlook und andere clients  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Zugriffstyp:  <br/> |Nur-Lese- oder Lese-/Schreibzugriff, je nach Speicheranbieter  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMAPIProp: IUnknown](imapipropiunknown.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren. Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben. [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag. Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:
  
|||
|:-----|:-----|
|x LpGuid:  <br/> |PSETID_Common  <br/> |
|UlKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "NoFolderScan"  <br/> |
   
Diese Eigenschaft bietet eine Möglichkeit für Anbieter, um Outlook anzugeben, nicht zum Scannen Kontakteordner im Speicher um eine leistungsbeeinträchtigung zu vermeiden. Es wird im Seriendruck-Vorgänge in denen Outlook überprüft das Vorhandensein und der Wert dieser Eigenschaft verwendet, bevor Sie mit der Überprüfung.
  
Standardmäßig ist diese Eigenschaft nicht in einem Speicher verfügbar gemacht bedeutet, dass Outlook den Ordner Kontakte für den Speicher gescannt werden kann. Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden die möglichen Werte:
  
- Null (0): Outlook kann die Überprüfung ausführen.
    
- Wert ungleich NULL: Outlook sollte Kontakteordner im Store nicht überprüft.
    

