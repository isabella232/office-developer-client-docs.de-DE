---
title: PidTagAttachRendering (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a1df3ba8e57f1e91894b88d7e8a72feb681e13dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794116"
---
# <a name="pidtagattachrendering-canonical-property"></a>PidTagAttachRendering (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Eine Microsoft Windows-Metadatei mit Informationen für eine Anlage enthält. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_RENDERING  <br/> |
|Bezeichner:  <br/> |0x3709  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Zweck dieser Eigenschaft ist ein Symbol oder andere bildliche Darstellung, die innerhalb der übergeordneten Nachricht zum Zeitpunkt der Anlage angezeigt werden kann. Diese Darstellung umfasst in der Regel den Namen der Anlage, falls vorhanden, und die Art der Anlage, wie beispielsweise Microsoft Office Word-Dokument. Eine Clientanwendung können diese Darstellung in der Anzeige der Nachricht. 
  
Bei einer Anlage dargestellt ist diese Eigenschaft in der Regel ein Symbol für die Datei. 
  
Diese Eigenschaft ist für eine angefügte Nachricht in der Regel nicht festgelegt. Eine Clientanwendung zum Rendern einer angefügten Nachricht benötigen sollte seine Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) zu erhalten, rufen Sie [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) für einen Zeiger auf das entsprechende Informationen Formularobjekt, Öffnen Sie die [IMAPIFormInfo](imapiforminfoimapiprop.md) -Benutzeroberfläche für dieses Objekt und verwenden Sie **GetProps** zum Abrufen des **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))-Eigenschaft. 
  
Bei einem eingebetteten statische OLE-Objekt enthält diese Eigenschaft eine Microsoft Windows-Metadatei, die verwendet werden kann, um die Darstellung der Anlage in einem Fenster zeichnen. 
  
Der Client sollte für ein eingebettetes dynamische OLE-Objekt OLE-Daten verwenden, um die Wiedergabe von Informationen zu generieren. 
  
In allen Fällen beachten die Clientanwendung Sie, dass diese Eigenschaft in der Regel mehrere hundert Bytes in Größe ist und Abschneiden in der Tabelle Dateianhang unterliegt. Wenn ein Client die Anlage aus dieser Eigenschaft Rendern möchte, ohne die Anlage selbst zu öffnen, müssen sie innerhalb der Tabelle abschneiden Regel arbeiten. Weitere Informationen finden Sie unter [Arbeiten mit großen Spalten](working-with-large-columns.md). 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

