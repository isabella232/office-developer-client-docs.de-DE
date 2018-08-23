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
ms.openlocfilehash: b9166090321aa24e35fe1c82908aec0c403095cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593739"
---
# <a name="launching-a-form-to-read-a-message"></a>Starten eines Formulars zum Lesen einer Nachricht

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Formular Server Implementierer erwarten, die folgende Sequenz von Methode Anrufe an ihre Formular Server- und Formularobjekte beim Laden von einer Clientanwendung aus einer Nachricht:
  
1. Die Clientanwendung wird den Formular-Manager mit einem Aufruf der Funktion [MAPIOpenFormMgr](mapiopenformmgr.md) geöffnet. 
    
2. Die Clientanwendung ruft die [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) -Methode, die ein [IMAPIForm](imapiformiunknown.md)-Objekt zurückgibt. Der Formular-Manager kann jetzt freigegeben werden muss, wenn es nicht für weitere Formular Aktivierungen verwendet werden soll. Beachten Sie, dass ein Aufruf von **LoadForm** einige Zeit dauern, da der Formular-Manager möglicherweise zum Installieren des Servers, der das Formular ausführbare Dateien vor dem fortfahren. 
    
3. Optional kann die Clientanwendung [IMAPIViewContext](imapiviewcontextiunknown.md) Steuerelement Schritten vorbereiten, die das Form-Objekt geladen werden die vorherige oder nächste Nachricht im Ordner führen kann. Die Client-Anwendung können die [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) -Methode den Standard-Ansichtskontext ändern, die festgelegt wurde in den Anruf **LoadForm** . 
    
4. Die Clientanwendung ruft die [IPersistMessage::Load](ipersistmessage-load.md) -Methode, um Meldungsdaten in das Form-Objekt zu laden. 
    
5. Die Clientanwendung ruft [IMAPIForm::DoVerb](imapiform-doverb.md) zum Aufrufen der open Verbs Zeiger der optionalen [IMAPIViewContext](imapiviewcontextiunknown.md) -Schnittstelle übergeben. 
    
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

