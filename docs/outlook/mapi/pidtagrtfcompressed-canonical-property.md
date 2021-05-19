---
title: PidTagRtfCompressed (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357890"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>PidTagRtfCompressed (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Rich Text Format (RTF)-Version des Nachrichtentexts, in der Regel in komprimierter Form. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RTF_COMPRESSED  <br/> |
|Kennung:  <br/> |0x1009  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |E-Mails  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft enthält denselben Nachrichtentext wie die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft, aber in RTF. 
  
Nachrichtentext in RTF wird normalerweise in komprimierter Form gespeichert. In einigen Systemen wird formatierter Text jedoch nicht komprimiert. Um sie zu unterstützen, stellt MAPI den wert dwMagicUncompressedRTF für einen Datenstromheader zur Identifizierung nicht komprimierter RTF und das **STORE_UNCOMPRESSED_RTF-Flag** in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) für den Nachrichtenspeicher zur Angabe, dass nicht komprimiertes RTF gespeichert werden kann. 
  
Um den Inhalt dieser Eigenschaft zu erhalten, rufen **Sie OpenProperty** auf, und rufen Sie [wrapCompressedRTFStream](wrapcompressedrtfstream.md) mit dem MAPI_READ **auf.** Um in diese Eigenschaft zu schreiben, öffnen Sie sie **mit** den MAPI_MODIFY und **MAPI_CREATE** Flags. Dadurch wird sichergestellt, dass die neuen Daten alle alten Daten vollständig ersetzen und dass die Schreibvorgänge mithilfe der Mindestanzahl von Speicherupdates ausgeführt werden. 
  
Nachrichtenspeicher, die RTF unterstützen, ignorieren alle Änderungen an Leerzeichen im Nachrichtentext. Wenn **PR_BODY** zum ersten Mal gespeichert wird, generiert und speichert der Nachrichtenspeicher auch diese Eigenschaft. Wenn die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) anschließend aufgerufen wird und **PR_BODY** geändert wurde, ruft der Nachrichtenspeicher die [RTFSync-Funktion](rtfsync.md) auf, um die Synchronisierung mit der RTF-Version sicherzustellen. Wenn nur Leerzeichen geändert wurden, bleiben die Eigenschaften unverändert. Dadurch wird jede nichttriviale RTF-Formatierung beibehalten, wenn die Nachricht über nicht RTF-wahrneige Clients und Messagingsysteme geht. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Codiert und decodiert einen komprimierten Datenstrom in RTF-Nachrichtentexten.
    
[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Kapselt zusätzliche Inhaltsformate (z. B. HTML) innerhalb der RTF-Body-Eigenschaft von Nachrichten und Anlagen.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

