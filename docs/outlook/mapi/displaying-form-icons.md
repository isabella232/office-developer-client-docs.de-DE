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
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438631"
---
# <a name="displaying-form-icons"></a>Anzeigen von Formularsymbolen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Anzeigen einer Liste von Nachrichten in einem Ordner ist es für Ihre Benutzer hilfreich, wenn Sie Nachrichten mit benutzerdefinierten Nachrichtenklassen vom standardmäßigen IPM unterscheiden. Notieren Sie sich Nachrichten. Benutzerdefinierte Nachrichtenklassen entsprechen Formularservern, und Formularserver stellen Symbole für sich selbst zur Verfügung. Sie können diese Symbole in der Liste der Nachrichten anzeigen, um Benutzer vor dem Öffnen der Nachrichten vor der Nachrichtenklasse der einzelnen Nachrichten zu warnen. In der Regel ist das Symbol in der **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))-Eigenschaft das Symbol, das in der Liste der Nachrichten angezeigt werden sollte. Formulare verfügen auch **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) -Eigenschaft, die angezeigt werden kann, wenn das Formular in einem Eigenschaftenblatt minimiert wird.
  
 **So erhalten Sie ein Symbol für eine Nachrichtenklasse, ohne den Formularserver für diese Nachrichtenklasse zu aktivieren**
  
1. Rufen Sie [die IMAPIFormMgr::OpenFormContainer-Methode](imapiformmgr-openformcontainer.md) auf, um einen Zeiger auf eine [IMAPIFormContainer : IUnknown-Schnittstelle zu](imapiformcontaineriunknown.md) erhalten. 
    
2. Rufen Sie [die IMAPIFormContainer::ResolveMessageClass-Methode](imapiformcontainer-resolvemessageclass.md) auf, um einen Zeiger auf eine [IMAPIFormInfo : IMAPIProp-Schnittstelle zu](imapiforminfoimapiprop.md) erhalten. 
    
3. Rufen Sie [die IMAPIFormInfo::MakeIconFromBinary-Methode](imapiforminfo-makeiconfrombinary.md) auf, um ein Symbolhandle zu erhalten. 
    
Das Symbol kann dann mit standardmäßigen Win32-APIs angezeigt werden.
  
> [!IMPORTANT]
> Sobald Sie über das Symbol für eine Nachrichtenklasse verfügen, müssen Sie alles tun, um dieses Symbol zwischenspeichern. Das Zwischenspeichern von Symbolen hat schwerwiegende Auswirkungen auf die Leistung von Clientanwendungen. Achten Sie beim Zwischenspeichern von Symbolen auf die Beziehungen zwischen Nachrichtenklassen und ihren Unterklassen. Beispiel: Wenn das IPM. Note.Meeting.Cancel-Nachrichtenklasse wird wieder in IPM aufgelöst. Beachten Sie, dass nicht alle Unterklassen von IPM angenommen werden. Hinweis sollte das Symbol für IPM verwenden. Hinweis. 
  

