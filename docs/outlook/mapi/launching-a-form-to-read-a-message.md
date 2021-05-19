---
title: Starten eines Formulars zum Lesen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 439927dc78941f086c025d77c76236497d3f4a15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425932"
---
# <a name="launching-a-form-to-read-a-message"></a>Starten eines Formulars zum Lesen einer Nachricht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Implementierung von Formularservern sollte die folgende Abfolge von Methodenaufrufen an ihren Formularserver und Formularobjekte erwarten, wenn eine Clientanwendung eine Nachricht lädt:
  
1. Die Clientanwendung öffnet den Formular-Manager mit einem Aufruf der [MAPIOpenFormMgr-Funktion.](mapiopenformmgr.md) 
    
2. Die Clientanwendung ruft die [IMAPIFormMgr::LoadForm-Methode](imapiformmgr-loadform.md) auf, die ein Objekt mit [IMAPIForm zurückgibt.](imapiformiunknown.md) Der Formular-Manager kann jetzt freigegeben werden, wenn er nicht für weitere Formularaktivierungen verwendet wird. Beachten Sie, dass ein Aufruf von **LoadForm** einige Zeit dauern kann, da der Formular-Manager möglicherweise die ausführbaren Dateien des Formularservers installieren muss, bevor er fortfahren kann. 
    
3. Optional kann die Clientanwendung [IMAPIViewContext](imapiviewcontextiunknown.md) vorbereiten, um Vorgänge zu steuern, die dazu führen können, dass das Formularobjekt die vorherige oder nächste Nachricht in den Ordner laden kann. Die Clientanwendung kann die [IMAPIForm::SetViewContext-Methode](imapiform-setviewcontext.md) verwenden, um den Standardansichtskontext zu ändern, der im **LoadForm-Aufruf festgelegt** wurde. 
    
4. Die Clientanwendung ruft die [IPersistMessage::Load-Methode](ipersistmessage-load.md) auf, um Nachrichtendaten in das Formularobjekt zu laden. 
    
5. Die Clientanwendung ruft [IMAPIForm::D oVerb](imapiform-doverb.md) auf, um das geöffnete Verb auf aufruft, und übergeben dabei den optionalen [IMAPIViewContext-Schnittstellenzeiger.](imapiviewcontextiunknown.md) 
    
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

