---
title: Anzeigen von Formularsymbolen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2b7177c72d1d60d75c64bfaaf5e85fba46c4aa3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551678"
---
# <a name="displaying-form-icons"></a>Anzeigen von Formularsymbolen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Anzeigen einer Liste von Nachrichten in einem Ordner ist es für Ihre Benutzer hilfreich, wenn Sie Nachrichten mit benutzerdefinierten Nachrichtenklassen vom Standard-IPM unterscheiden. Notieren Sie sich Nachrichten. Benutzerdefinierte Nachrichtenklassen entsprechen Formularservern, und Formularserver stellen Symbole zur Darstellung bereit. Sie können diese Symbole in der Liste der Nachrichten anzeigen, um Benutzer auf die Nachrichtenklasse jeder Nachricht hinzuweisen, bevor der Benutzer die Nachrichten öffnet. In der Regel ist das Symbol in der **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) -Eigenschaft des Formulars das Symbol, das in der Liste der Nachrichten angezeigt werden soll. Formulare verfügen auch über eine **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) -Eigenschaft, die angezeigt werden kann, wenn das Formular in einem Eigenschaftenblatt minimiert wird.
  
 **So rufen Sie ein Symbol für eine Nachrichtenklasse ab, ohne den Formularserver für diese Nachrichtenklasse zu aktivieren**
  
1. Rufen Sie die [IMAPIFormMgr::OpenFormContainer-Methode](imapiformmgr-openformcontainer.md) auf, um einen Zeiger auf eine [IMAPIFormContainer : IUnknown-Schnittstelle](imapiformcontaineriunknown.md) abzurufen. 
    
2. Rufen Sie die [IMAPIFormContainer::ResolveMessageClass-Methode](imapiformcontainer-resolvemessageclass.md) auf, um einen Zeiger auf eine [IMAPIFormInfo : IMAPIProp-Schnittstelle](imapiforminfoimapiprop.md) abzurufen. 
    
3. Rufen Sie die [IMAPIFormInfo::MakeIconFromBinary-Methode](imapiforminfo-makeiconfrombinary.md) auf, um ein Symbolhandle abzurufen. 
    
Das Symbol kann dann mit win32-Standard-APIs angezeigt werden.
  
> [!IMPORTANT]
> Sobald Sie das Symbol für eine Nachrichtenklasse haben, versuchen Sie, dieses Symbol zwischenzuspeichern. Das Zwischenspeichern von Symbolen wirkt sich nicht stark auf die Leistung von Clientanwendungen aus. Achten Sie beim Zwischenspeichern von Symbolen auf die Beziehungen zwischen Nachrichtenklassen und deren Unterklassen. Beispiel: IPM. Note.Meeting.Cancel message class happens to resolve back to IPM. Beachten Sie, dass nicht davon ausgegangen wird, dass alle Unterklassen von IPM. Beachten Sie, dass Sie das Symbol für IPM verwenden sollten. Hinweis. 
  

