---
title: Display Server Folder Sizes-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434550"
---
# <a name="display-server-folder-sizes-property"></a>Display Server Folder Sizes-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt die Größe der angegebenen Ordner auf dem Server im Dialogfeld Outlook **Ordnergröße** an. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Verfügbar gemacht für:  <br/> |[IMsgStore : IMAPIProp-Objekt](imsgstoreimapiprop.md)  <br/> |
|Erstellt von:  <br/> |Store Anbieter  <br/> |
|Zugriff durch:  <br/> |Outlook und andere Clients  <br/> |
|Eigenschaftstyp:  <br/> |PT_BOOLEAN  <br/> |
|Zugriffstyp:  <br/> |Lesen/Schreiben  <br/> |
   
## <a name="remarks"></a>Hinweise

Um eine der Speicherfunktionen bereitzustellen, muss der Speicheranbieter [IMAPIProp : IUnknown](imapipropiunknown.md) implementieren und ein gültiges Eigenschaftstag für eine dieser Eigenschaften zurückgeben, die an einen [IMAPIProp::GetIDsFromNames-Aufruf](imapiprop-getidsfromnames.md) übergeben werden. Wenn das Eigenschaftstag für eine dieser Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss der Speicheranbieter auch den richtigen Eigenschaftswert zurückgeben. Store können [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) aufrufen, um diese Eigenschaften zu erhalten oder zu festlegen. 
  
Zum Abrufen des Werts dieser Eigenschaft sollte der Client zunächst [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) verwenden, um das Eigenschaftstag abzurufen, und dann dieses Eigenschaftstag in [IMAPIProp::GetProps](imapiprop-getprops.md) angeben, um den Wert abzurufen. Geben Sie beim Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)die folgenden Werte für die [MAPINAMEID-Struktur](mapinameid.md) an, auf die der Eingabeparameter _lppPropNames verweist:_
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"  <br/> |
   
Diese Eigenschaft wird in Microsoft Outlook 2003 Service Pack (SP) 1 unterstützt. Wenn die Version von Outlook vor Outlook 2003 SP 1 liegt oder der Wert **false** ist, zeigt Outlook nur die Größe der Ordner im lokalen Speicher an. Wenn diese Eigenschaft für einen Speicher festgelegt ist, der Outlook 2003 SP 1 verwendet, wird von Outlook die Größe der einzelnen angegebenen Ordner auf dem Server und dem lokalen Laufwerk abgefragt. 
  
Zum Abfragen der Ordnergröße auf dem Server öffnet Outlook einen Ordner im Speicher mit [IMsgStore::OpenEntry,](imsgstore-openentry.md)übergeben das Flag **MAPI_NO_CACHE**, und fragt dann nach PR_MESSAGE_SIZE_EXTENDED **.** Der Speicheranbieter sollte dann die Ordnergröße auf dem Server zurückgeben.
  
Um die Größe eines Ordners auf dem lokalen Laufwerk zu abfragen, öffnet Outlook den Ordner ohne **MAPI_NO_CACHE** Flag. Anschließend werden Abfragen für **PR_MESSAGE_SIZE_EXTENDED**; Der Speicheranbieter sollte die Größe des angegebenen Ordners auf dem lokalen Laufwerk zurückgeben.
  
Mit diesem Eigenschaftensatz können Anbieter, die Speicherinhalte mit einem Server synchronisieren, Im Dialogfeld Ordnergröße auf dem Server Outlook **Ordnergröße** anzeigen. Benutzer können dann ihre aktuelle Serverspeichernutzung mit Serverkontingenten vergleichen. 
  

