---
title: Anzeigen von Formular Symbolen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337044"
---
# <a name="displaying-form-icons"></a>Anzeigen von Formular Symbolen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie eine Liste von Nachrichten in einem Ordner anzeigen, ist es für Ihre Benutzer hilfreich, wenn Sie Nachrichten mit benutzerdefinierten Nachrichtenklassen vom standardmäßigen IPM unterscheiden. Hinweis Nachrichten. Benutzerdefinierte Nachrichtenklassen entsprechen Formular Servern, und Formularserver stellen Symbole bereit, die sich selbst darstellen. Sie können diese Symbole in der Liste der Nachrichten anzeigen, um die Benutzer für die Nachrichtenklasse der einzelnen Nachrichten zu benachrichtigen, bevor der Benutzer die Nachricht öffnet. In der Regel ist das Symbol in der **PR_MINI_ICON** ([pidtagminiicon (](pidtagminiicon-canonical-property.md))-Eigenschaft des Formulars diejenige, die in der Liste der Nachrichten angezeigt werden soll. Formulare verfügen außerdem über eine **PR_ICON** ([pidtagicon (](pidtagicon-canonical-property.md))-Eigenschaft, die angezeigt werden kann, wenn das Formular in einem Eigenschaftenfenster minimiert wird.
  
 **So rufen Sie ein Symbol für eine Nachrichtenklasse ab, ohne den Formularserver für diese Nachrichtenklasse zu aktivieren**
  
1. Rufen Sie die [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) -Methode auf, um einen Zeiger auf eine [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) -Schnittstelle abzurufen. 
    
2. Rufen Sie die [IMAPIFormContainer:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) -Methode auf, um einen Zeiger auf eine [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) -Schnittstelle abzurufen. 
    
3. Rufen Sie die [IMAPIFormInfo:: MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) -Methode auf, um ein Symbol-Handle abzurufen. 
    
Das Symbol kann dann mit standardmäßigen Win32-APIs angezeigt werden.
  
> [!IMPORTANT]
> Sobald Sie das Symbol für eine Nachrichtenklasse haben, sollten Sie das Symbol Zwischenspeichern. Nicht zwischenspeichernde Symbole haben gravierende Auswirkungen auf die Leistung von Clientanwendungen. Achten Sie beim Zwischenspeichern von Symbolen auf die Beziehungen zwischen Nachrichtenklassen und ihren Unterklassen. Wenn beispielsweise die IPM. Note. Meeting. Cancel-Nachrichtenklasse wird wieder in IPM aufgelöst. Beachten Sie, dass alle Unterklassen von IPM. Hinweis sollte das Symbol für IPM verwenden. Hinweis. 
  

