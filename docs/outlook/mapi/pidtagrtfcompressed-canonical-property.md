---
title: Kanonische PidTagRtfCompressed-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357890"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>Kanonische PidTagRtfCompressed-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die RTF-Version (Rich Text Format) des Nachrichtentexts in der Regel in komprimierter Form. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RTF_COMPRESSED  <br/> |
|Kennung:  <br/> |0x1009  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |E-Mail  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält denselben Nachrichtentext wie die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft, aber in RTF. 
  
Der Nachrichtentext in RTF wird normalerweise in komprimierter Form gespeichert. Einige Systeme komprimieren jedoch keinen formatierten Text. Um diese zu erfüllen, stellt MAPI den dwMagicUncompressedRTF-Wert für einen Stream-Header bereit, um unkomprimiertes RTF zu identifizieren, und das **STORE_UNCOMPRESSED_RTF** -Flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) für die Nachricht. Speicher, um anzugeben, dass unkomprimiertes RTF gespeichert werden kann. 
  
Um den Inhalt dieser Eigenschaft abzurufen, rufen Sie **openProperty**auf, und rufen Sie dann [WrapCompressedRTFStream](wrapcompressedrtfstream.md) mit dem **MAPI_READ** -Flag auf. Um in diese Eigenschaft zu schreiben, öffnen Sie Sie mit den **MAPI_MODIFY** -und **MAPI_CREATE** -Flags. Dadurch wird sichergestellt, dass die neuen Daten alle alten Daten vollständig ersetzen und die Schreibvorgänge mit der Mindestanzahl von Speicher Updates ausgeführt werden. 
  
Nachrichtenspeicher, die RTF unterstützen, ignorieren alle Änderungen an Leerzeichen im Nachrichtentext. Wenn **PR_BODY** zum ersten Mal gespeichert wird, generiert und speichert der Nachrichtenspeicher diese Eigenschaft. Wenn die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode anschließend aufgerufen wird und **PR_BODY** geändert wurde, ruft der Nachrichtenspeicher die [RTFSync](rtfsync.md) -Funktion auf, um die Synchronisierung mit der RTF-Version sicherzustellen. Wenn nur Leerraum geändert wurde, bleiben die Eigenschaften unverändert. Dadurch werden alle nicht trivialen RTF-Formatierungen beibehalten, wenn die Nachricht über nicht-RTF-fähige Clients und Messagingsysteme reist. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Codiert und dekodiert einen komprimierten Stream in RTF-Nachrichtentexten.
    
[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Kapselt zusätzliche Inhaltsformate (wie HTML) innerhalb der RTF-Text Eigenschaft von Nachrichten und Anlagen.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

