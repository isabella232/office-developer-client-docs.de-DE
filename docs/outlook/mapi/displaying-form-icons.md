---
title: Anzeigen von Formularsymbolen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7ac8026489b06031e07ab4b2978c9ece04063bb1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579144"
---
# <a name="displaying-form-icons"></a>Anzeigen von Formularsymbolen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beim Anzeigen einer Liste von Nachrichten in einem Ordner ist es hilfreich, die Benutzer, wenn Sie von der standardmäßigen IPM Nachrichten mit benutzerdefinierten Nachrichtenklassen unterscheiden. Beachten Sie Nachrichten. Benutzerdefinierte Nachrichtenklassen entsprechen den Formular-Servern und Formular Server bieten Symbole, um sich selbst darstellen. Sie können diese Symbole in der Liste der Nachrichten an Benutzer zu jeder Nachricht Nachrichtenklasse anzeigen, bevor der Benutzer die Nachrichten öffnet. Das Symbol in das Formular **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))-Eigenschaft ist in der Regel diejenige, die in der Liste der Nachrichten angezeigt werden soll. Formulare enthalten auch eine **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md))-Eigenschaft, die angezeigt werden, wenn das Formular in einem Eigenschaftenfenster minimiert ist.
  
 **Um ein Symbol für eine Nachrichtenklasse zu erhalten, ohne Aktivieren der Formular-Servers für die Nachrichtenklasse**
  
1. Rufen Sie die [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) -Methode, um einen Zeiger auf eine [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) Schnittstelle. 
    
2. Rufen Sie die [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) -Methode, um einen Zeiger auf eine [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) Schnittstelle. 
    
3. Rufen Sie die [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) -Methode, um ein Symbolhandle abzurufen. 
    
Das Symbol kann mit standard Win32-APIs angezeigt werden.
  
> [!IMPORTANT]
> Nachdem Sie das Symbol für eine Nachrichtenklasse haben, stellen Sie bemüht, Symbol zwischengespeichert. Zwischenspeichern von Symbolen nicht schwerwiegend wirkt sich auf die Leistung von Clientanwendungen aus. Beim Zwischenspeichern von Symbolen, achten Sie auf die Beziehungen zwischen Nachrichtenklassen und ihre Unterklassen. Angenommen, wenn die IPM. Note.Meeting.Cancel Nachrichtenklasse geschieht mit wieder auf IPM zu beheben. Beachten Sie, nicht angenommen wird, die alle Unterklassen IPM. Hinweis sollte das Symbol für IPM verwendet werden. Beachten Sie. 
  

