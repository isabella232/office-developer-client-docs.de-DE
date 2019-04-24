---
title: VerFassen einer neuen Nachricht mithilfe eines Formulars
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335126"
---
# <a name="composing-a-new-message-by-using-a-form"></a>VerFassen einer neuen Nachricht mithilfe eines Formulars

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um ein Formular zum Verfassen einer neuen Nachricht zu verwenden, erstellen Sie zunächst ein neues benutzerdefiniertes Nachrichtenobjekt.
  
 **So erstellen Sie eine neue Nachricht mithilfe eines Formulars**
  
1. Rufen Sie die [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode des Formular-Managers auf, um einen Zeiger auf ein Form Information-Objekt abzurufen – ein Objekt, das die [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) -Schnittstelle implementiert. 
    
2. Führen Sie den Zeiger in einem Aufruf von [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md)an das Formular Informationsobjekt weiter. **CreateForm** lädt den entsprechenden Formularserver. Geben Sie darüber hinaus einen Schnittstellenbezeichner an **CreateForm** an, um die Schnittstelle anzugeben, die für den Zugriff auf die neue Nachricht verwendet werden soll. In der Regel fordern Sie [IPersistMessage: IUnknown](ipersistmessageiunknown.md) an, indem **** Sie IID_IPersistMessage an CreateForm übergeben.
    
3. Speichern Sie die neue Nachricht, indem Sie die [IPersistMessage:: Save](ipersistmessage-save.md) -Methode aufrufen. Der Formularserver sollte beim Erstellen der Nachricht Werte für die erforderlichen Eigenschaften der Nachricht festlegen. 
    
4. Laden Sie die Nachricht mit einer der beiden folgenden Strategien: [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) oder [IMAPISession::P Repareform](imapisession-prepareform.md) gefolgt von [IMAPISession:: ShowForm](imapisession-showform.md). Weitere Informationen zu diesen Strategien finden Sie unter [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md).
    
> [!NOTE]
> Es gibt Möglichkeiten für Leistungsverbesserungen beim Laden einer neuen benutzerdefinierten Nachricht in einen Formularserver, da Sie bereits über die Möglichkeit zum Abrufen von Informationen zu der Nachricht (beispielsweise der Nachrichtenklasse) während der für die ** ResolveMessageClass** - **** und CreateForm-Aufrufe. Aus diesem Grund können Sie die erforderliche Verarbeitung vereinfachen, bevor Sie **LoadForm** aufrufen, die im Thema [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md)beschrieben werden. 
  

