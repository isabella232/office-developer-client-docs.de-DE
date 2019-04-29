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
  
Formularserver Implementierer sollten die folgende Abfolge von Methoden aufrufen zu ihren Formularserver-und Formularobjekten erwarten, wenn eine Clientanwendung eine Nachricht lädt:
  
1. Die Clientanwendung öffnet den Formular-Manager mit einem Aufruf der [MAPIOpenFormMgr](mapiopenformmgr.md) -Funktion. 
    
2. Die Clientanwendung Ruft die [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) -Methode auf, die ein Objekt mit [IMAPIForm](imapiformiunknown.md)zurückgibt. Der Formular-Manager kann jetzt veröffentlicht werden, wenn er nicht für weitere Formular Aktivierungen verwendet wird. Beachten Sie, dass ein Aufruf von **LoadForm** möglicherweise einige Zeit in Anspruch nimmt, da der Formular-Manager die ausführbaren Dateien des Formular Servers möglicherweise installieren muss, bevor Sie fortfahren. 
    
3. Optional kann die Clientanwendung [IMAPIViewContext](imapiviewcontextiunknown.md) vorbereiten, um Vorgänge zu steuern, die dazu führen können, dass das Formularobjekt die vorherige oder nächste Nachricht im Ordner lädt. Die Clientanwendung kann die [IMAPIForm::](imapiform-setviewcontext.md) setviewcontext-Methode verwenden, um den Standard Ansichtskontext zu ändern, der im **LoadForm** -Aufruf festgelegt wurde. 
    
4. Die Clientanwendung Ruft die [IPersistMessage:: Laden](ipersistmessage-load.md) -Methode auf, um Nachrichtendaten in das Form-Objekt zu laden. 
    
5. Die Clientanwendung Ruft [IMAPIForm::D overb](imapiform-doverb.md) auf, um das Open-Verb aufzurufen, wobei der optionale [IMAPIViewContext](imapiviewcontextiunknown.md) -Schnittstellenzeiger übergeben wird. 
    
## <a name="see-also"></a>Siehe auch



[Formular Server interAktionen](form-server-interactions.md)

