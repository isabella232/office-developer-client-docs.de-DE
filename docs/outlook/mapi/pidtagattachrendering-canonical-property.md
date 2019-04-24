---
title: Kanonische Pidtagattachrendering (-Eigenschaft
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
ms.openlocfilehash: 22d3e649641dbe688912ecece7fde73a555f4a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361096"
---
# <a name="pidtagattachrendering-canonical-property"></a>Kanonische Pidtagattachrendering (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Microsoft Windows-Metadatei mit Renderinginformationen für eine Anlage. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_RENDERING  <br/> |
|Kennung:  <br/> |0x3709  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Zweck dieser Eigenschaft besteht darin, ein Symbol oder eine andere bildliche Darstellung bereitzustellen, die in der übergeordneten Nachricht am Punkt der Anlage angezeigt werden kann. Eine solche Darstellung enthält in der Regel den Namen der Anlage, falls vorhanden, und die Art der Anlage, wie beispielsweise ein Microsoft Office Word-Dokument. Eine Clientanwendung kann diese Darstellung in der Anzeige der Nachricht verwenden. 
  
Für eine angefügte Datei wird in der Regel ein Symbol für die Datei dargestellt. 
  
Für eine angefügte Nachricht ist diese Eigenschaft in der Regel nicht festgelegt. Eine Clientanwendung, die eine angefügte Nachricht Rendern muss, sollte Ihre **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft aufrufen [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) für einen Zeiger auf das entsprechende Formular Informationsobjekt, Öffnen Sie die [IMAPIFormInfo](imapiforminfoimapiprop.md) -Schnittstelle für dieses Objekt, und verwenden Sie GetProps, um die **PR_ICON** ([pidtagicon (](pidtagicon-canonical-property.md)) oder **PR_MINI_ICON** ([pidtagminiicon (](pidtagminiicon-canonical-property.md))-Eigenschaft abzurufen. **** 
  
Bei einem eingebetteten statischen OLE-Objekt enthält diese Eigenschaft eine Microsoft Windows-Metadatei, die zum Zeichnen der Anlagendarstellung in einem Fenster verwendet werden kann. 
  
Bei einem eingebetteten dynamischen OLE-Objekt sollte der Client die OLE-Daten verwenden, um die Renderinginformationen zu generieren. 
  
In allen Fällen sollte die Clientanwendung beachten, dass diese Eigenschaft in der Regel mehrere hundert Bytes groß ist und in der Attachment-Tabelle abgeschnitten wird. Wenn ein Client die Anlage aus dieser Eigenschaft Rendern möchte, ohne die Anlage selbst zu öffnen, muss Sie innerhalb der Tabellen Kürzungs Regel funktionieren. Weitere Informationen finden Sie unter [Arbeiten mit umfangreichen Spalten](working-with-large-columns.md). 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
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

