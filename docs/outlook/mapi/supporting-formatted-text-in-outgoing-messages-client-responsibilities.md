---
title: Unterstützung von formatierten Text in ausgehenden Nachrichten Client Zuständigkeiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 975dd172b6ad342351f014d0966d62a150f713c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571290"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Unterstützung von formatiertem Text in ausgehenden Nachrichten: Kundenaufgaben

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen legen Sie die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft, die Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) oder die **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** ([PidTagHtml](pidtaghtml-canonical-property.md))-Eigenschaft für eine ausgehende Nachricht. Clients, die nur-Text unterstützen festlegen nur die **PR_BODY** -Eigenschaft. Rich-Text-Format (RTF)-fähigen Clients möglicherweise **PR_BODY** und **PR_RTF_COMPRESSED** Eigenschaften festlegen oder nur **PR_RTF_COMPRESSED**, je nach der Nachricht Speicheranbieter verwendet wird. HTML-fähigen Clients festlegen die **http://Schemas.Microsoft.com/mapi/proptag/0x10130102** -Eigenschaft. 
  
Es ist wichtig, damit ein Client überprüfen Sie den Nachrichtenspeicher **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft, um festzustellen, ob der Informationsspeicher RTF unterstützt. Ist der Nachrichtenspeicher nicht RTF-fähigen, legt ein RTF-fähigen Client die **PR_BODY** und die **PR_RTF_COMPRESSED** Eigenschaften für jede ausgehende Nachricht fest. 
  
Wenn der Nachrichtenspeicher RTF-fähigen ist, muss nur die **PR_RTF_COMPRESSED** -Eigenschaft festgelegt werden soll. 
  
 **Zum Festlegen von PR_RTF_COMPRESSED und stellen Sie sicher, dass die Synchronisierung geschieht als erforderlich, RTF-fähigen clients**
  
1. Rufen Sie die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, um die **PR_RTF_COMPRESSED** -Eigenschaft festlegen der MAPI_CREATE ist und die MAPI_MODIFY Flags zu öffnen. MAPI_CREATE ist sichergestellt, dass neuen Daten alle alten Daten ersetzt und MAPI_MODIFY ermöglicht es Ihnen, diese Ersetzung vornehmen. 
    
2. Rufen Sie die [WrapCompressedRTFStream](wrapcompressedrtfstream.md) -Funktion, und übergeben Sie STORE_UNCOMPRESSED_RTF des Nachrichtenspeichers das STORE_UNCOMPRESSED_RTF Bit in seiner **PR_STORE_SUPPORT_MASK** -Eigenschaft, um einen nicht komprimierten Version der **PR_RTF_COMPRESSED abrufen festgelegt **Stream von **OpenProperty**zurückgegeben.
    
3. Schreiben Sie die Meldungsdaten Text in der nicht komprimierten Stream von **WrapCompressedRTFStream**zurückgegeben.
    
4. Commit, und der nicht komprimierten und komprimierte Streams freigeben.
    
Zu diesem Zeitpunkt, wenn der Nachricht Speicheranbieter RTF unterstützt, haben Sie alle durchgeführt, die erforderlich ist. Sie können die Nachricht Speicheranbieter Synchronisierungsvorgangs und die Erstellung der **PR_BODY** -Eigenschaft behandelt werden sollen bei Bedarf abhängen. Jedoch müssen der Nachricht Speicheranbieter RTF nicht unterstützt, Sie die [RTFSync](rtfsync.md) -Funktion, um den Text mit der Formatierung synchronisieren aufrufen, das RTF_SYNC_RTF_CHANGED-Flag festlegen. 
  

