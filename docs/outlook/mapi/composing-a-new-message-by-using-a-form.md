---
title: Verfassen einer neuen Nachricht mithilfe eines Formulars
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412800"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Verfassen einer neuen Nachricht mithilfe eines Formulars

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um ein Formular zum Verfassen einer neuen Nachricht zu verwenden, erstellen Sie zunächst ein neues benutzerdefiniertes Nachrichtenobjekt.
  
 **So verfassen Sie eine neue Nachricht mithilfe eines Formulars**
  
1. Rufen Sie die [IMAPIFormMgr::ResolveMessageClass-Methode](imapiformmgr-resolvemessageclass.md) des Formular-Managers auf, um einen Zeiger auf ein Formularinformationsobjekt abzurufen – ein Objekt, das die [IMAPIFormInfo : IMAPIProp-Schnittstelle](imapiforminfoimapiprop.md) implementiert. 
    
2. Übergeben Sie den Zeiger an das Formularinformationsobjekt in einem Aufruf von [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm** lädt den entsprechenden Formularserver. Übergeben Sie außerdem eine Schnittstellen-ID an **CreateForm,** um die Schnittstelle anzugeben, die für den Zugriff auf die neue Nachricht verwendet werden soll. In der Regel fordern Sie [IPersistMessage : IUnknown](ipersistmessageiunknown.md) an, indem Sie IID_IPersistMessage **CreateForm übergeben.**
    
3. Speichern Sie die neue Nachricht, indem Sie die [IPersistMessage::Save-Methode](ipersistmessage-save.md) aufrufen. Der Formularserver sollte beim Erstellen der Nachricht Werte für die erforderlichen Eigenschaften der Nachricht festlegen. 
    
4. Laden Sie die Nachricht mithilfe einer von zwei Strategien: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) oder [IMAPISession::P repareForm](imapisession-prepareform.md) gefolgt von [IMAPISession::ShowForm](imapisession-showform.md). Weitere Informationen zu diesen Strategien finden Sie unter [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md).
    
> [!NOTE]
> Es gibt Möglichkeiten für Leistungsgewinne beim Laden einer neuen benutzerdefinierten Nachricht auf einem Formularserver, da Sie bereits während der Verarbeitung, die für die **ResolveMessageClass-** und **CreateForm-Aufrufe** erforderlich ist, die Möglichkeit hatten, Informationen zur Nachricht – z. B. der Nachrichtenklasse – zu erhalten. Aus diesem Grund können Sie die Verarbeitung vereinfachen, bevor **Sie LoadForm über** das im Thema Laden einer Nachricht in ein Formular beschriebene Aufrufen [aufrufen.](loading-a-message-into-a-form.md) 
  

