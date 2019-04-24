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
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="6b6a2-103">VerFassen einer neuen Nachricht mithilfe eines Formulars</span><span class="sxs-lookup"><span data-stu-id="6b6a2-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="6b6a2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b6a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b6a2-105">Um ein Formular zum Verfassen einer neuen Nachricht zu verwenden, erstellen Sie zunächst ein neues benutzerdefiniertes Nachrichtenobjekt.</span><span class="sxs-lookup"><span data-stu-id="6b6a2-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="6b6a2-106">**So erstellen Sie eine neue Nachricht mithilfe eines Formulars**</span><span class="sxs-lookup"><span data-stu-id="6b6a2-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="6b6a2-107">Rufen Sie die [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode des Formular-Managers auf, um einen Zeiger auf ein Form Information-Objekt abzurufen – ein Objekt, das die [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="6b6a2-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="6b6a2-108">Führen Sie den Zeiger in einem Aufruf von [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md)an das Formular Informationsobjekt weiter.</span><span class="sxs-lookup"><span data-stu-id="6b6a2-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="6b6a2-109">**CreateForm** lädt den entsprechenden Formularserver.</span><span class="sxs-lookup"><span data-stu-id="6b6a2-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="6b6a2-110">Geben Sie darüber hinaus einen Schnittstellenbezeichner an **CreateForm** an, um die Schnittstelle anzugeben, die für den Zugriff auf die neue Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b6a2-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="6b6a2-111">In der Regel fordern Sie [IPersistMessage: IUnknown](ipersistmessageiunknown.md) an, indem \*\*\*\* Sie IID_IPersistMessage an CreateForm übergeben.</span><span class="sxs-lookup"><span data-stu-id="6b6a2-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="6b6a2-112">Speichern Sie die neue Nachricht, indem Sie die [IPersistMessage:: Save](ipersistmessage-save.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6b6a2-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="6b6a2-113">Der Formularserver sollte beim Erstellen der Nachricht Werte für die erforderlichen Eigenschaften der Nachricht festlegen.</span><span class="sxs-lookup"><span data-stu-id="6b6a2-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="6b6a2-114">Laden Sie die Nachricht mit einer der beiden folgenden Strategien: [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) oder [IMAPISession::P Repareform](imapisession-prepareform.md) gefolgt von [IMAPISession:: ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="6b6a2-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="6b6a2-115">Weitere Informationen zu diesen Strategien finden Sie unter [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="6b6a2-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="6b6a2-116">Es gibt Möglichkeiten für Leistungsverbesserungen beim Laden einer neuen benutzerdefinierten Nachricht in einen Formularserver, da Sie bereits über die Möglichkeit zum Abrufen von Informationen zu der Nachricht (beispielsweise der Nachrichtenklasse) während der für die \*\* ResolveMessageClass\*\* - \*\*\*\* und CreateForm-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="6b6a2-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="6b6a2-117">Aus diesem Grund können Sie die erforderliche Verarbeitung vereinfachen, bevor Sie **LoadForm** aufrufen, die im Thema [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6b6a2-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

