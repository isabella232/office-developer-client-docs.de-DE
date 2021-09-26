---
title: Erstellen einer neuen Nachricht mithilfe eines Formulars
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4356fadc307ce260315a306693ef18e348722485
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611035"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Erstellen einer neuen Nachricht mithilfe eines Formulars

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um ein Formular zum Verfassen einer neuen Nachricht zu verwenden, erstellen Sie zuerst ein neues benutzerdefiniertes Nachrichtenobjekt.
  
 **So verfassen Sie eine neue Nachricht mithilfe eines Formulars**
  
1. Rufen Sie die [IMAPIFormMgr::ResolveMessageClass-Methode](imapiformmgr-resolvemessageclass.md) des Formular-Managers auf, um einen Zeiger auf ein Formularinformationsobjekt abzurufen – ein Objekt, das die [IMAPIFormInfo : IMAPIProp-Schnittstelle](imapiforminfoimapiprop.md) implementiert. 
    
2. Übergeben Sie den Zeiger an das Formularinformationsobjekt in einem Aufruf von [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm** lädt den entsprechenden Formularserver. Übergeben Sie außerdem einen Schnittstellenbezeichner an **CreateForm,** um die Schnittstelle anzugeben, die für den Zugriff auf die neue Nachricht verwendet werden soll. In der Regel fordern Sie [IPersistMessage : IUnknown](ipersistmessageiunknown.md) an, indem Sie IID_IPersistMessage an **CreateForm** übergeben.
    
3. Speichern Sie die neue Nachricht, indem Sie die [IPersistMessage::Save-Methode](ipersistmessage-save.md) aufrufen. Der Formularserver sollte Werte für die erforderlichen Eigenschaften der Nachricht festlegen, wenn er die Nachricht erstellt. 
    
4. Laden Sie die Nachricht mithilfe einer von zwei Strategien: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) oder [IMAPISession::P repareForm](imapisession-prepareform.md) gefolgt von [IMAPISession::ShowForm](imapisession-showform.md). Weitere Informationen zu diesen Strategien finden Sie unter [Laden einer Nachricht in ein Formular.](loading-a-message-into-a-form.md)
    
> [!NOTE]
> Es gibt Möglichkeiten für Leistungsvorteile beim Laden einer neuen benutzerdefinierten Nachricht in einen Formularserver, da Sie bereits während der Verarbeitung, die für **resolveMessageClass-** und **CreateForm-Aufrufe** erforderlich ist, Informationen über die Nachricht erhalten haben, z. B. die Nachrichtenklasse. Aus diesem Grund können Sie die Verarbeitung vereinfachen, die erforderlich ist, bevor Sie LoadForm über die im Thema [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md)beschriebene Aufrufen von **LoadForm** aufrufen. 
  

