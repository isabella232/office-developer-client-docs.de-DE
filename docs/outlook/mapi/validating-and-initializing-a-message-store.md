---
title: Überprüfen und Initialisieren einer Nachricht Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2c8bf46bd9328d1e9da975c9fd39dbdf75605e5a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619484"
---
# <a name="validating-and-initializing-a-message-store"></a>Überprüfen und Initialisieren einer Nachricht Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie einen Nachrichtenspeicher über die [IMAPISession::OpenMsgStore-Methode](imapisession-openmsgstore.md) öffnen, ohne das MDB_NO_MAIL-Flag festzulegen, erstellt MAPI mehrere Ordner und weist ihnen Standardnamen und -rollen zu. MapI ist für das Erstellen dieser Ordner verantwortlich, um die Inkompatibilitäten zu vermeiden, die zwangsläufig auftreten würden, wenn Clients oder Nachrichtenspeicheranbieter für die Erstellung verantwortlich wären. 
  
Manchmal muss überprüft werden, ob die entsprechenden Ordner erstellt wurden und gültig sind. Die [HrValidateIPMSubtree-Funktion](hrvalidateipmsubtree.md) ist für diesen Zweck verfügbar. Wenn Sie den Standardnachrichtenspeicher überprüfen, übergeben Sie das flag MAPI_FULL_IPM_TREE. Für den Standardnachrichtenspeicher wird eine umfangreichere Gruppe von Ordnern erstellt. Wenn **HrValidateIPMSubtree** das flag MAPI_FULL_IPM_TREE erhält, wird nach den folgenden Ordnern gesucht: 
  
- Stammordner für die IPM-Unterstruktur
    
- Ordner "Gelöschte Elemente" im IPM-Stammordner
    
- Posteingangsordner im IPM-Stammordner
    
- Postausgangsordner im IPM-Stammordner
    
- Ordner "Gesendete Elemente" im IPM-Stammordner
    
- Ordneransichten im Stammordner des Nachrichtenspeichers
    
- Allgemeine Ansichten im Stammordner des Nachrichtenspeichers
    
- Suchordner im Stammordner des Nachrichtenspeichers
    
Wenn der Nachrichtenspeicher nicht standardmäßig ist, können Sie das MAPI_FULL_IPM_TREE Flag entweder festlegen oder nicht festlegen. Wenn dieses Kennzeichen nicht festgelegt ist, überprüft **HrValidateIPMSubtree** nur den Stammordner für die Unterstruktur, den Ordner "Gelöschte Elemente" und den Stammordner für die Suchergebnisse des Nachrichtenspeichers. 
  
Um einen Nachrichtenspeicher zu initialisieren, speichern Sie die folgenden Eigenschaften im Speicher, damit sie verfügbar sind:
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Diese Eigenschaften sind Bitmasken, die Features des Nachrichtenspeichers beschreiben. **PR_VALID_FOLDER_MASK** hat für jeden speziellen Ordner, der im Nachrichtenspeicher vorhanden ist, ein Bit festgelegt und einen gültigen Eintragsbezeichner zugewiesen. Weitere Informationen zum Zugriff auf diese Ordner und deren Eintragsbezeichner finden Sie unter [Öffnen einer Nachricht Store Ordners.](opening-a-message-store-folder.md) 
  
 **PR_STORE_SUPPORT_MASK** hat für jedes feature, das im Nachrichtenspeicher unterstützt wird, ein Bit festgelegt. Wenn z. B. ein Nachrichtenspeicher Benachrichtigungen und formatierten Text unterstützt, sind **für die PR_STORE_SUPPORT_MASK** die STORE_NOTIFY_OK und STORE_RTF_OK Bits festgelegt. 
  
Andere Eigenschaften, die lokal gespeichert werden sollen, sind die Eintragsbezeichner für die Ordner, die die **PR_VALID_FOLDER_MASK-Eigenschaft** als gültig beschreibt. Jedem dieser speziellen Ordner mit Ausnahme des Ordners Posteingang ist eine Eintragsbezeichnereigenschaft zugeordnet. Der Eintragsbezeichner für den Ordner "Postausgang" ist beispielsweise die **eigenschaft PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). Da es sich bei diesen Ordnern um die Ordner handelt, die häufig geöffnet werden, empfiehlt es sich, die Eintragsbezeichner sofort verfügbar zu machen.
  

