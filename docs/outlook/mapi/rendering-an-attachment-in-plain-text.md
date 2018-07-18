---
title: Darstellen einer Anlage als Nur-Text
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 38db1d18f240188c7566a57afa23291a307446dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795381"
---
# <a name="rendering-an-attachment-in-plain-text"></a>Darstellen einer Anlage als Nur-Text

  
  
**Betrifft**: Outlook 
  
Um eine Anlage in einer Nachricht mit nur-Text zu rendern, rufen Sie die Anlage **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft, und wenden sie auf die Daten in der **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) -Eigenschaft. Es gibt zwei Methoden, um **PR_RENDERING_POSITION**abzurufen:
  
- Öffnen Sie die Anlage durch Aufrufen der Nachricht **IMessage::OpenAttach** -Methode, und bitten Sie durch Aufrufen der Anlage **IMAPIProp::GetProps** -Methode für die **PR_RENDERING_POSITION** -Eigenschaft. Weitere Informationen finden Sie unter [IMessage::OpenAttach](imessage-openattach.md) und [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Rufen Sie die Nachricht **IMessage::GetAttachmentTable** -Methode zum Zugriff auf die Anlagentabelle und Abrufen der Spalte, die die **PR_RENDERING_POSITION** -Eigenschaft enthält. Auf diese Weise ist immer vorzuziehen. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
Beachten Sie, dass viele RTF-fähigen Nachrichtenspeicher **PR_RENDERING_POSITION** nicht berechnet werden, bis ein Client die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft einer Nachricht anfordert beibehalten. Bis dahin stellt **PR_RENDERING_POSITION** in der Regel ein Näherungswert. Nachricht Anbieter dürfen die Clients mit ungefährer Wert zur Verbesserung der Leistung bereitstellen. 
  
Das Rendering für eine Datei oder binäre Anlage wird in seiner **PR_ATTACH_RENDERING** -Eigenschaft gespeichert. Sie haben die Wahl des Abrufen von **PR_ATTACH_RENDERING** auf die gleiche Weise, wie Sie **PR_RENDERING_POSITION**abgerufen: direkt aus der Anlage oder aus der Anlagentabelle. Für **PR_ATTACH_RENDERING**, die erste Strategie, obwohl zeitaufwändiger, sicherer ist. Da einige Anbieter Nachricht ihre Tabellenspalten auf 255 Byte oder in einigen Fällen 510 Bytes abschneiden, ist es schwierig, um sicherzustellen, dass die Spalte **PR_ATTACH_RENDERING** das vollständige Rendering enthält. Wenn die Eigenschaft direkt über das Attachment-Objekt abgerufen wird, wird es immer abgeschlossen sein. 
  
OLE weder Nachricht Anlagen festlegen **PR_ATTACH_RENDERING**. Stattdessen wird in der Nachricht Textstream Renderinginformationen für Anlagen OLE 1 gespeichert. Für Anlagen der OLE-2 wird es in einen Datenstrom spezielle untergeordnete Speicherobjekt gespeichert. Rendern von Informationen für e-Mail-Anlagen kann über den Formular-Manager. 
  
 **Das Rendering für e-Mail-Anlagen abrufen**
  
1. Verwenden Sie die Nachrichtenklasse der Nachricht, um den Formular-Manager zuzugreifen.
    
2. Der Formular-Manager **PR_MINI_ICON** -Eigenschaft zugreifen. Weitere Informationen finden Sie unter **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).
    

