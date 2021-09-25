---
title: PidTagAttachRendering (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0571d7726c17334867138346f92e99deccf9f259
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600456"
---
# <a name="pidtagattachrendering-canonical-property"></a>PidTagAttachRendering (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Microsoft Windows-Metadatei mit Renderinginformationen für eine Anlage. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_RENDERING  <br/> |
|Kennung:  <br/> |0x3709  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Zweck dieser Eigenschaft besteht darin, ein Symbol oder eine andere bildliche Darstellung bereitzustellen, die innerhalb der übergeordneten Nachricht am Punkt der Anlage angezeigt werden kann. Eine solche Darstellung umfasst in der Regel den Namen der Anlage, falls vorhanden, und die Art der Anlage, z. B. ein Microsoft Office Word-Dokument. Eine Clientanwendung kann diese Darstellung in der Anzeige der Nachricht verwenden. 
  
Bei einer angefügten Datei erhält diese Eigenschaft in der Regel ein Symbol für die Datei. 
  
Bei einer angefügten Nachricht ist diese Eigenschaft in der Regel nicht festgelegt. Eine Clientanwendung, die eine angefügte Nachricht rendern muss, sollte ihre **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft abrufen, [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) für einen Zeiger auf das entsprechende Formularinformationsobjekt aufrufen, die [IMAPIFormInfo-Schnittstelle](imapiforminfoimapiprop.md) für dieses Objekt öffnen und **GetProps** verwenden, um die **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) oder **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) -Eigenschaft abzurufen. 
  
Für ein eingebettetes statisches OLE-Objekt enthält diese Eigenschaft eine Microsoft Windows Metadatei, die zum Zeichnen der Anlagendarstellung in einem Fenster verwendet werden kann. 
  
Für ein eingebettetes dynamisches OLE-Objekt sollte der Client die OLE-Daten verwenden, um die Renderinginformationen zu generieren. 
  
In allen Fällen sollte die Clientanwendung beachten, dass diese Eigenschaft in der Regel mehrere hundert Bytes groß ist und in der Anlagentabelle abgeschnitten wird. Wenn ein Client die Anlage aus dieser Eigenschaft rendern möchte, ohne die Anlage selbst zu öffnen, muss sie innerhalb der Tabellenkürzungsregel funktionieren. Weitere Informationen finden Sie unter [Arbeiten mit großen Spalten.](working-with-large-columns.md) 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
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

