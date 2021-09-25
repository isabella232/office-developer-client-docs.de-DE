---
title: Display Server Folder Sizes-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de408d947228100553a7768b36882c3c9c3518fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584584"
---
# <a name="display-server-folder-sizes-property"></a>Display Server Folder Sizes-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt die Größe der angegebenen Ordner auf dem Server im Dialogfeld Outlook **Ordnergröße** an. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar gemacht für:  <br/> |[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)  <br/> |
|Erstellt von:  <br/> |Store Anbieter  <br/> |
|Zugriff von:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschaftentyp:  <br/> |PT_BOOLEAN  <br/> |
|Zugriffstyp:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMAPIProp : IUnknown](imapipropiunknown.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden. Wenn das Eigenschaftentag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben. Store Anbieter können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften abzurufen oder festzulegen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zuerst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter  _"lppPropNames"_ zeigt:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"  <br/> |
   
Diese Eigenschaft wird in Microsoft Outlook 2003 Service Pack (SP) 1 unterstützt. Wenn die Version von Outlook älter als Outlook 2003 SP 1 ist oder der Wert **"false"** lautet, zeigt Outlook nur die Ordnergrößen im lokalen Speicher an. Wenn diese Eigenschaft für einen Speicher festgelegt ist, der Outlook 2003 SP 1 verwendet, wird Outlook die Größe jedes angegebenen Ordners auf dem Server und des lokalen Laufwerks abfragen. 
  
Zum Abfragen der Ordnergröße auf dem Server öffnet Outlook einen Ordner im Speicher mit [IMsgStore::OpenEntry,](imsgstore-openentry.md)übergibt das Flag **MAPI_NO_CACHE** und fragt dann **PR_MESSAGE_SIZE_EXTENDED** ab. Der Speicheranbieter sollte dann die Ordnergröße auf dem Server zurückgeben.
  
Zum Abfragen der Größe eines Ordners auf dem lokalen Laufwerk öffnet Outlook den Ordner ohne das **flag MAPI_NO_CACHE.** Anschließend wird nach **PR_MESSAGE_SIZE_EXTENDED** abgefragt; Der Speicheranbieter sollte die Größe des angegebenen Ordners auf dem lokalen Laufwerk zurückgeben.
  
Mit diesem Eigenschaftensatz können Speicheranbieter, die Speicherinhalte mit einem Server synchronisieren, Ordnergrößendaten auf dem Server im Dialogfeld Outlook **Ordnergröße** anzeigen. Benutzer können dann ihre aktuelle Serverspeichernutzung mit Serverkontingenten vergleichen. 
  

