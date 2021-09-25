---
title: PidTagRtfCompressed (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b762ca668ecc52b2a9a354bbde2a5e8abb923906
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555097"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>PidTagRtfCompressed (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die RTF-Version (Rich Text Format) des Nachrichtentexts, in der Regel in komprimierter Form. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RTF_COMPRESSED  <br/> |
|Kennung:  <br/> |0x1009  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |E-Mails  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft enthält den gleichen Nachrichtentext wie die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft, aber in RTF. 
  
Nachrichtentext in RTF wird normalerweise in komprimierter Form gespeichert. Einige Systeme komprimieren jedoch keinen formatierten Text. Um sie zu berücksichtigen, stellt MAPI den wetterMagicUncompressedRTF-Wert für einen Streamheader bereit, um nicht komprimierte RTF zu identifizieren, und das **flag STORE_UNCOMPRESSED_RTF** in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), damit der Nachrichtenspeicher nicht komprimiertes RTF speichern kann. 
  
Rufen Sie zum Abrufen des Inhalts dieser Eigenschaft **OpenProperty** auf, und rufen Sie [wrapCompressedRTFStream](wrapcompressedrtfstream.md) mit dem **flag MAPI_READ** auf. Um in diese Eigenschaft zu schreiben, öffnen Sie sie mit den **Flags MAPI_MODIFY** und **MAPI_CREATE.** Dadurch wird sichergestellt, dass die neuen Daten alle alten Daten vollständig ersetzen und dass die Schreibvorgänge mithilfe der mindesten Anzahl von Speicherupdates ausgeführt werden. 
  
Nachrichtenspeicher, die RTF unterstützen, ignorieren alle Änderungen an Leerzeichen im Nachrichtentext. Wenn **PR_BODY** zum ersten Mal gespeichert wird, wird diese Eigenschaft auch vom Nachrichtenspeicher generiert und gespeichert. Wenn die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) anschließend aufgerufen wird und **PR_BODY** geändert wurde, ruft der Nachrichtenspeicher die [RTFSync-Funktion](rtfsync.md) auf, um die Synchronisierung mit der RTF-Version sicherzustellen. Wenn nur Leerzeichen geändert wurden, bleiben die Eigenschaften unverändert. Dadurch bleiben alle nichttrivialen RTF-Formatierungen erhalten, wenn die Nachricht nicht RTF-fähige Clients und Messagingsysteme durchsucht. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Codiert und decodiert einen komprimierten Datenstrom in RTF-Nachrichtentexten.
    
[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Kapselt zusätzliche Inhaltsformate (z. B. HTML) innerhalb der RTF-Texteigenschaft von Nachrichten und Anlagen.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

