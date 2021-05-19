---
title: Überprüfen und Initialisieren einer Nachricht Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433689"
---
# <a name="validating-and-initializing-a-message-store"></a>Überprüfen und Initialisieren einer Nachricht Store

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie einen Nachrichtenspeicher über die [IMAPISession::OpenMsgStore-Methode](imapisession-openmsgstore.md) öffnen, ohne das MDB_NO_MAIL-Flag zu setzen, erstellt MAPI mehrere Ordner und weist ihnen Standardnamen und Rollen zu. MAPI ist für das Erstellen dieser Ordner verantwortlich, um die Inkompatibilitäten zu vermeiden, die zwangsläufig auftreten würden, wenn entweder Clients oder Nachrichtenspeicheranbieter für die Erstellung verantwortlich wären. 
  
Manchmal muss überprüft werden, ob die entsprechenden Ordner erstellt wurden und gültig sind. Die [HrValidateIPMSubtree-Funktion](hrvalidateipmsubtree.md) ist zu diesem Zweck verfügbar. Wenn Sie den Standardnachrichtenspeicher überprüfen, übergeben Sie das MAPI_FULL_IPM_TREE. Für den Standardnachrichtenspeicher wird eine umfangreichere Gruppe von Ordnern erstellt. Wenn **HrValidateIPMSubtree** das MAPI_FULL_IPM_TREE erhält, wird nach den folgenden Ordnern überprüft: 
  
- Stammordner für die IPM-Unterstruktur
    
- Ordner "Gelöschte Elemente" im IPM-Stammordner
    
- Posteingangsordner im IPM-Stammordner
    
- Ordner "Outbox" im IPM-Stammordner
    
- Ordner "Gesendete Elemente" im IPM-Stammordner
    
- Ordneransichten im Stammordner des Nachrichtenspeichers
    
- Allgemeine Ansichten im Stammordner des Nachrichtenspeichers
    
- Suchordner im Stammordner des Nachrichtenspeichers
    
Wenn der Nachrichtenspeicher nicht die Standardeinstellung ist, können Sie das MAPI_FULL_IPM_TREE festlegen. Wenn dieses Flag nicht festgelegt ist, sucht **HrValidateIPMSubtree** nur nach dem Stammordner für die Unterstruktur, den Ordner "Gelöschte Elemente" und den Stammordner für Die Suchergebnisse des Nachrichtenspeichers. 
  
Zum Initialisieren eines Nachrichtenspeichers speichern Sie die folgenden Eigenschaften im Arbeitsspeicher, sodass sie sofort verfügbar sind:
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Diese Eigenschaften sind Bitmasken, die Features des Nachrichtenspeichers beschreiben. **PR_VALID_FOLDER_MASK** für jeden speziellen Ordner, der im Nachrichtenspeicher vorhanden ist, und über einen zugewiesenen Eintragsbezeichner verfügt, der gültig ist, ist ein Bit festgelegt. Weitere Informationen zum Zugriff auf diese Ordner und deren Eintragsbezeichner finden Sie unter [Opening a Message Store Folder](opening-a-message-store-folder.md). 
  
 **PR_STORE_SUPPORT_MASK** ist für jedes feature, das im Nachrichtenspeicher unterstützt wird, ein Bit festgelegt. Wenn beispielsweise ein Nachrichtenspeicher Benachrichtigungen und  formatierten Text unterstützt, PR_STORE_SUPPORT_MASK die STORE_NOTIFY_OK und STORE_RTF_OK festgelegt. 
  
Zu den anderen Eigenschaften, die lokal gespeichert werden sollen, gehören die Eintragsbezeichner für die Ordner, die von **der PR_VALID_FOLDER_MASK** als gültig beschrieben werden. Jedem dieser speziellen Ordner, mit Ausnahme des Posteingangsordners, ist eine Eintrags-ID-Eigenschaft zugeordnet. Der Eintragsbezeichner für den Ordner "Outbox" ist beispielsweise die **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) -Eigenschaft. Da es sich bei diesen Ordnern um die Ordner handelt, die häufig geöffnet werden, ist es eine gute Idee, die Eintrags-IDs sofort verfügbar zu machen.
  

