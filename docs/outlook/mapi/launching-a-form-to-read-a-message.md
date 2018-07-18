---
title: Starten eines Formulars zum Lesen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 675de7eeda534d8761887cdcb6d5c94a209ca18b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792895"
---
# <a name="launching-a-form-to-read-a-message"></a>Starten eines Formulars zum Lesen einer Nachricht

  
  
**Betrifft**: Outlook 
  
Formular Server Implementierer erwarten, die folgende Sequenz von Methode Anrufe an ihre Formular Server- und Formularobjekte beim Laden von einer Clientanwendung aus einer Nachricht:
  
1. Die Clientanwendung wird den Formular-Manager mit einem Aufruf der Funktion [MAPIOpenFormMgr](mapiopenformmgr.md) geöffnet. 
    
2. Die Clientanwendung ruft die [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) -Methode, die ein [IMAPIForm](imapiformiunknown.md)-Objekt zurückgibt. Der Formular-Manager kann jetzt freigegeben werden muss, wenn es nicht für weitere Formular Aktivierungen verwendet werden soll. Beachten Sie, dass ein Aufruf von **LoadForm** einige Zeit dauern, da der Formular-Manager möglicherweise zum Installieren des Servers, der das Formular ausführbare Dateien vor dem fortfahren. 
    
3. Optional kann die Clientanwendung [IMAPIViewContext](imapiviewcontextiunknown.md) Steuerelement Schritten vorbereiten, die das Form-Objekt geladen werden die vorherige oder nächste Nachricht im Ordner führen kann. Die Client-Anwendung können die [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) -Methode den Standard-Ansichtskontext ändern, die festgelegt wurde in den Anruf **LoadForm** . 
    
4. Die Clientanwendung ruft die [IPersistMessage::Load](ipersistmessage-load.md) -Methode, um Meldungsdaten in das Form-Objekt zu laden. 
    
5. Die Clientanwendung ruft [IMAPIForm::DoVerb](imapiform-doverb.md) zum Aufrufen der open Verbs Zeiger der optionalen [IMAPIViewContext](imapiviewcontextiunknown.md) -Schnittstelle übergeben. 
    
## <a name="see-also"></a>Siehe auch



[Formularserverinteraktionen](form-server-interactions.md)

