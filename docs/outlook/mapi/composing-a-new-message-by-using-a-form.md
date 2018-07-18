---
title: Schreiben einer neuen Nachricht mit einem Formular
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f4b9cb00512838e6b54c0cc910b8f7279120db3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791425"
---
# <a name="composing-a-new-message-by-using-a-form"></a>Schreiben einer neuen Nachricht mit einem Formular

  
  
**Betrifft**: Outlook 
  
Um ein Formular zum Verfassen einer neuen Nachricht verwenden, müssen Sie zuerst erstellen Sie ein neue benutzerdefinierte Message-Objekt.
  
 **Um eine neue Nachricht mit einem Formular zum Verfassen**
  
1. Rufen Sie den Formular-Manager [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode, um einen Zeiger auf ein Form-Informationsobjekt abzurufen – ein Objekt, das implementiert die [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) Schnittstelle. 
    
2. Übergeben Sie den Zeiger auf das Formular Informationen-Objekt in einem Aufruf von [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md). **CreateForm** lädt den entsprechende Formular Server. Übergeben Sie darüber hinaus Interface Identifier an **CreateForm** an, das die Schnittstelle für die neue Nachricht Zugriff auf verwendet werden. In der Regel, die Sie anfordern [IPersistMessage: IUnknown](ipersistmessageiunknown.md) , indem Sie auf **CreateForm**IID_IPersistMessage übergeben.
    
3. Speichern Sie die neue Nachricht durch seine [IPersistMessage::Save](ipersistmessage-save.md) -Methode aufrufen. Der Formular-Server sollte Werte für die Nachricht erforderlichen Eigenschaften festgelegt, wenn die Nachricht erstellt. 
    
4. Laden Sie die Nachricht mithilfe einer der beiden folgenden Strategien: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) oder [IMAPISession::PrepareForm](imapisession-prepareform.md) gefolgt von [IMAPISession::ShowForm](imapisession-showform.md). Weitere Informationen zu diesen Strategien finden Sie unter [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md).
    
> [!NOTE]
> Möglichkeiten zur Leistungssteigerung vorhanden sind, eine neue benutzerdefinierte Meldung in einem Formular Server zu laden, da Sie bereits Gelegenheit, einige Informationen über die Meldung erhalten kommuniziert haben, werden – wie deren Nachrichtenklasse – während der Verarbeitung für die **erforderlich ResolveMessageClass** und **CreateForm** Anrufe. Aus diesem Grund werden Sie vereinfachen die Verarbeitung vor dem Aufruf von **LoadForm** , die in den in der [Nachricht in ein Formular geladen](loading-a-message-into-a-form.md)Thema beschriebenen erforderlich sein. 
  

