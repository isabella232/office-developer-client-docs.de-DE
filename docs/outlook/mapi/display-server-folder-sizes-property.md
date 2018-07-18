---
title: Eigenschaft zum Anzeigen von Serverordnergrößen
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1ddf4501918d598169a3a74fd1c8d2ac38499cd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791552"
---
# <a name="display-server-folder-sizes-property"></a>Eigenschaft zum Anzeigen von Serverordnergrößen

  
  
**Betrifft**: Outlook 
  
Zeigt die Größe der angegebenen Ordner auf dem Server im Dialogfeld Outlook- **Ordner-Größe** . 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Eingeblendet auf:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Objekt  <br/> |
|Erstellt:  <br/> |Speicheranbieter  <br/> |
|Durch zugegriffen:  <br/> |Outlook und andere clients  <br/> |
|Der Eigenschaftentyp:  <br/> |PT_BOOLEAN  <br/> |
|Zugriffstyp:  <br/> |Lese-/Schreibzugriff  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um die Store-Funktionalität bereitzustellen, Speicheranbieter implementieren muss [IMAPIProp: IUnknown](imapipropiunknown.md) und ein Tag valid-Eigenschaft für alle diese Eigenschaften übergeben Sie einen Anruf [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) zurückzukehren. Wenn das Eigenschafts-Tag für alle diese Eigenschaften an [IMAPIProp::GetProps](imapiprop-getprops.md)übergeben wird, muss Speicheranbieter auch den richtige Wert zurückgeben. [HrGetOneProp](hrgetoneprop.md) und [HrSetOneProp](hrsetoneprop.md) , zum Abrufen oder Festlegen dieser Eigenschaften Anbieter aufgerufen. 
  
Um den Wert dieser Eigenschaft abzurufen, sollte der Client zunächst mit dem [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) um das Eigenschafts-Tag zu erhalten und geben Sie in [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen des Werts dieser Eigenschaftentag. Beim Aufruf von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), geben Sie die folgenden Werte für die [MAPINAMEID](mapinameid.md) -Struktur an, das Eingabeparameter _LppPropNames_auf zeigt:
  
|||
|:-----|:-----|
|x LpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|UlKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "Urn: Schemas-Microsoft-Com:office:outlook #serverfoldersizes"  <br/> |
   
Diese Eigenschaft wird in Microsoft Outlook 2003 Service Pack (SP) 1 unterstützt. Wenn die Version von Outlook einer älteren Version als Outlook 2003 SP 1 ist, oder wenn der Wert **false**lautet, Outlook nur die Größe der Ordner auf dem lokalen Speicher zeigt. Wenn diese Eigenschaft in einem Speicher festgelegt ist, Outlook 2003 SP 1 verwendet, wird die Größe der einzelnen angegebenen Ordner auf dem Server und dem lokalen Laufwerk Outlook Abfragen. 
  
Um die Größe des Ordners auf dem Server abzufragen, Outlook wird geöffnet, einen Ordner auf den Speicher mit [IMsgStore::OpenEntry](imsgstore-openentry.md), übergeben die Kennzeichen **MAPI_NO_CACHE**, und fragt dann **PR_MESSAGE_SIZE_EXTENDED**. Der Anbieter sollte die Größe des Ordners klicken Sie dann auf dem Server zurückgegeben.
  
Um die Größe eines Ordners auf dem lokalen Laufwerk abzufragen, öffnet Outlook den Ordner ohne das **MAPI_NO_CACHE** -Flag. Anschließend fragt **PR_MESSAGE_SIZE_EXTENDED**; der Anbieter sollte die Größe des angegebenen Ordners auf dem lokalen Laufwerk zurückgegeben werden.
  
Diese Eigenschaft festgelegt ist können Anbieter, die Store Inhalt auf einen Server synchronisieren Ordner Größendaten auf dem Server im Dialogfeld Outlook- **Größe des Ordners** anzeigen. Benutzer können ihre aktuellen Server Speicherplatzverwendung mit Vorgaben Server verglichen. 
  

