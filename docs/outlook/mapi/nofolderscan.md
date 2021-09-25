---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f4c08ccffa90702f9e5cbd532445ed6f38f342d5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556014"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob Microsoft Office Outlook Kontakteordner in einem Speicher überprüfen soll.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar gemacht für:  <br/> |[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)  <br/> |
|Erstellt von:  <br/> |Store Anbieter  <br/> |
|Zugriff von:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschaftentyp:  <br/> |PT_LONG  <br/> |
|Zugriffstyp:  <br/> |Schreibgeschützt oder Lese-/Schreibzugriff je nach Store-Anbieter  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMAPIProp : IUnknown](imapipropiunknown.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden. Wenn das Eigenschaftentag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben. Store Anbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter  _"lppPropNames"_ zeigt:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"NoFolderScan"  <br/> |
   
Diese Eigenschaft bietet Speicheranbietern die Möglichkeit, anzugeben, Outlook keine Kontakteordner im Speicher scannen, um Leistungseinbußen zu vermeiden. Es wird in Seriendruckvorgängen verwendet, bei denen Outlook vor dem Initiieren der Überprüfung das Vorhandensein und den Wert dieser Eigenschaft überprüft.
  
Diese Eigenschaft wird standardmäßig nicht für einen Speicher verfügbar gemacht, was bedeutet, dass Outlook den Ordner "Kontakte" im Speicher überprüfen können. Wenn die Eigenschaft verfügbar gemacht wird, sind die folgenden Werte möglich:
  
- Null (0): Outlook können den Scan ausführen.
    
- Wert ungleich Null: Outlook sollten keine Kontakteordner im Speicher überprüfen.
    

