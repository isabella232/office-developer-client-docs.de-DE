---
title: Starten eines Formulars zum Lesen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d12801658fde2155367090f48d23ca969f39b8fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561313"
---
# <a name="launching-a-form-to-read-a-message"></a>Starten eines Formulars zum Lesen einer Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formularserver implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:
  
1. Die Clientanwendung öffnet den Formular-Manager mit einem Aufruf der [MAPIOpenFormMgr-Funktion.](mapiopenformmgr.md) 
    
2. Die Clientanwendung ruft die [IMAPIFormMgr::LoadForm-Methode](imapiformmgr-loadform.md) auf, die ein Objekt mit [IMAPIForm](imapiformiunknown.md)zurückgibt. Der Formular-Manager wird möglicherweise jetzt freigegeben, wenn er nicht für weitere Formularaktivierungen verwendet wird. Beachten Sie, dass ein Aufruf von **LoadForm** einige Zeit in Anspruch nehmen kann, da der Formular-Manager möglicherweise die ausführbaren Dateien des Formularservers installieren muss, bevor er fortfahren kann. 
    
3. Optional kann die Clientanwendung [IMAPIViewContext](imapiviewcontextiunknown.md) vorbereiten, um Vorgänge zu steuern, die dazu führen können, dass das Formularobjekt die vorherige oder nächste Nachricht in den Ordner lädt. Die Clientanwendung kann die [IMAPIForm::SetViewContext-Methode](imapiform-setviewcontext.md) verwenden, um den Standardansichtskontext zu ändern, der im **LoadForm-Aufruf** festgelegt wurde. 
    
4. Die Clientanwendung ruft die [IPersistMessage::Load-Methode](ipersistmessage-load.md) auf, um Nachrichtendaten in das Formularobjekt zu laden. 
    
5. Die Clientanwendung ruft [IMAPIForm::D oVerb](imapiform-doverb.md) auf, um das geöffnete Verb aufzurufen, und übergibt den optionalen [IMAPIViewContext-Schnittstellenzeiger.](imapiviewcontextiunknown.md) 
    
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

