---
title: Erstellen eines einfachen E-Mail-Elements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8b7afa8f3c04cb479906f721db8de90e8cf66f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345193"
---
# <a name="create-a-simple-mail-item"></a><span data-ttu-id="12f85-103">Erstellen eines einfachen E-Mail-Elements</span><span class="sxs-lookup"><span data-stu-id="12f85-103">Create a simple mail item</span></span>
  
<span data-ttu-id="12f85-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12f85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12f85-105">MAPI kann verwendet werden, um eine Nachricht zu erstellen und zu senden, die eine Lesebestätigung anfordert.</span><span class="sxs-lookup"><span data-stu-id="12f85-105">MAPI can be used to create and send a message that requests a read receipt.</span></span> <span data-ttu-id="12f85-106">Wenn ein Lesebeleg angefordert wird, generiert und gibt das Messagingsystem einen Lesebericht an den Absender zurück, wenn der Empfänger die Nachricht öffnet.</span><span class="sxs-lookup"><span data-stu-id="12f85-106">When a read receipt is requested, the messaging system generates and returns a read report to the sender when the recipient opens the message.</span></span>
  
<span data-ttu-id="12f85-107">Informationen zum Herunterladen, Anzeigen und Ausführen des Codes aus der MFCMAPI-Anwendung und dem CreateOutlookItemsAddin-Projekt, auf das in diesem Thema verwiesen wird, finden Sie unter [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="12f85-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a><span data-ttu-id="12f85-108">So erstellen und senden Sie eine Nachricht, die eine Lesebestätigung anfordert</span><span class="sxs-lookup"><span data-stu-id="12f85-108">To create and send a message requesting a read receipt</span></span>

1. <span data-ttu-id="12f85-109">Erstellen Sie eine ausgehende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="12f85-109">Create an outgoing message.</span></span> <span data-ttu-id="12f85-110">Informationen zum Erstellen einer ausgehenden Nachricht finden Sie unter [Handling an Outgoing Message](handling-an-outgoing-message.md).</span><span class="sxs-lookup"><span data-stu-id="12f85-110">For information about how to create an outgoing message, see [Handling an Outgoing Message](handling-an-outgoing-message.md).</span></span>
    
2. <span data-ttu-id="12f85-111">Fügen Sie **die PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) -Eigenschaft hinzu, und legen Sie sie auf **true .**</span><span class="sxs-lookup"><span data-stu-id="12f85-111">Add the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and set it to **true**.</span></span>
    
3. <span data-ttu-id="12f85-112">Fügen Sie **die PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) -Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="12f85-112">Add the **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property.</span></span>
    
4. <span data-ttu-id="12f85-113">Fügen Sie **die PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) -Eigenschaft hinzu.</span><span class="sxs-lookup"><span data-stu-id="12f85-113">Add the **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) property.</span></span>
    
5. <span data-ttu-id="12f85-114">Senden Sie die Nachricht, indem Sie die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="12f85-114">Send the message by calling the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> 
    
<span data-ttu-id="12f85-115">Die  `AddMail` Funktion in der Quelldatei "Mails.cpp" des CreateOutlookItemsAddin-Projekts veranschaulicht diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="12f85-115">The  `AddMail` function in the Mails.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="12f85-116">Die Funktion übernimmt Parameter aus dem Dialogfeld E-Mail hinzufügen, das angezeigt wird, wenn Sie im Menü `AddMail` **Addins** in der  MFCMAPI-Beispielanwendung auf den Befehl E-Mail hinzufügen klicken. </span><span class="sxs-lookup"><span data-stu-id="12f85-116">The  `AddMail` function takes parameters from the **Add Mail** dialog box that is displayed when you click the **Add Mail** command on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="12f85-117">Die Funktion in Mails.cpp zeigt das Dialogfeld an und übergibt die Werte aus dem Dialogfeld  `DisplayAddMailDialog` an die  `AddMail` Funktion.</span><span class="sxs-lookup"><span data-stu-id="12f85-117">The  `DisplayAddMailDialog` function in Mails.cpp displays the dialog box and passes the values from the dialog box to the  `AddMail` function.</span></span> <span data-ttu-id="12f85-118">Die Funktion bezieht sich nicht direkt auf das Erstellen eines  `DisplayAddMailDialog` E-Mail-Elements mithilfe von MAPI, daher ist sie hier nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="12f85-118">The  `DisplayAddMailDialog` function does not relate directly to creating a mail item using MAPI, so it is not listed here.</span></span> <span data-ttu-id="12f85-119">Die  `AddMail` Funktion ist unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="12f85-119">The  `AddMail` function is listed below.</span></span> 
  
<span data-ttu-id="12f85-120">Beachten Sie, dass der an die Methode übergebene  _lpFolder-Parameter_ ein Zeiger auf eine  `AddMail` [IMAPIFolder-Schnittstelle](imapifolderimapicontainer.md) ist, die den Ordner darstellt, in dem die neue Nachricht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="12f85-120">Note that the  _lpFolder_ parameter passed to the  `AddMail` method is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new message will be created.</span></span> <span data-ttu-id="12f85-121">Angesichts des  _lpFolder-Parameters,_ der eine **IMAPIFolder-Schnittstelle** darstellt, ruft der Code die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) auf.</span><span class="sxs-lookup"><span data-stu-id="12f85-121">Given the  _lpFolder_ parameter that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="12f85-122">Die **CreateMessage-Methode** gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine [IMessage : IMAPIProp-Schnittstelle](imessageimapiprop.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="12f85-122">The **CreateMessage** method returns a success code and a pointer to a pointer to an [IMessage : IMAPIProp](imessageimapiprop.md) interface.</span></span> 

<span data-ttu-id="12f85-123">Der großteil des Funktionscodes übernimmt die Arbeit beim Festlegen von Eigenschaften in Vorbereitung auf den Aufruf der `AddMail` [IMAPIProp::SetProps-Methode.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="12f85-123">Most of the  `AddMail` function code handles the work of setting properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="12f85-124">Wenn der Aufruf der **SetProps-Methode** erfolgreich ist, werden bei einem Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) die Änderungen an den Speicher commits und ein neues E-Mail-Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="12f85-124">If the call to the **SetProps** method succeeds, a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method commits the changes to the store and creates a new mail item.</span></span> <span data-ttu-id="12f85-125">Wenn angefordert, wird dann die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufgerufen, um die Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="12f85-125">Then, if requested, the [IMessage::SubmitMessage](imessage-submitmessage.md) method is called to send the message.</span></span> 
  
<span data-ttu-id="12f85-126">Die Funktion verwendet zwei Hilfsfunktionen, um Werte für die Eigenschaften PR_CONVERSATION_INDEX und PR_REPORT_TAG zu `AddMail` erstellen: die   `BuildConversationIndex` `AddReportTag` und-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="12f85-126">The  `AddMail` function uses two helper functions to build values for the **PR_CONVERSATION_INDEX** and **PR_REPORT_TAG** properties: the  `BuildConversationIndex` and  `AddReportTag` functions.</span></span> <span data-ttu-id="12f85-127">Die Funktion in CreateOutlookItemsAddin.cpp führt die gleiche Arbeit aus wie die integrierte  `BuildConversationIndex` MAPI [ScCreateConversationIndex-Funktion,](sccreateconversationindex.md) wenn kein übergeordneter Unterhaltungsindex an sie übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="12f85-127">The  `BuildConversationIndex` function, located in CreateOutlookItemsAddin.cpp, does the same work that the built-in MAPI [ScCreateConversationIndex](sccreateconversationindex.md) function does when a parent conversation index is not passed to it.</span></span> <span data-ttu-id="12f85-128">Das Format des Unterhaltungsindexpuffers, den diese Funktionen generieren, ist in [der kanonischen Eigenschaft PidTagConversationIndex dokumentiert.](pidtagconversationindex-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="12f85-128">The format of the conversation index buffer that these functions generate is documented in [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md).</span></span> 

<span data-ttu-id="12f85-129">Die In Mails.cpp enthaltene Funktion ruft wiederum die Funktion auf, um eine Struktur für die PR_REPORT_TAG `AddReportTag` `BuildReportTag` erstellen. </span><span class="sxs-lookup"><span data-stu-id="12f85-129">The  `AddReportTag` function, located in Mails.cpp, in turn calls the  `BuildReportTag` function to build a structure for the **PR_REPORT_TAG** property.</span></span> <span data-ttu-id="12f85-130">Informationen zur Struktur, die die Funktion erstellt, finden Sie  `BuildReportTag` unter [PidTagReportTag Canonical Property](pidtagreporttag-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="12f85-130">For information about the structure that the  `BuildReportTag` function builds, see [PidTagReportTag Canonical Property](pidtagreporttag-canonical-property.md).</span></span>
  
<span data-ttu-id="12f85-131">Im Folgenden finden Sie die vollständige Auflistung der  `AddMail` Funktion.</span><span class="sxs-lookup"><span data-stu-id="12f85-131">The following is the complete listing of the  `AddMail` function.</span></span> 
  
```cpp
HRESULT AddMail(LPMAPISESSION lpMAPISession,
            LPMAPIFOLDER lpFolder,
            LPWSTR szSubject, // PR_SUBJECT_W, PR_CONVERSATION_TOPIC
            LPWSTR szBody, // PR_BODY_W
            LPWSTR szRecipientName, // Recipient table
            BOOL bHighImportance, // PR_IMPORTANCE
            BOOL bReadReceipt, // PR_READ_RECEIPT_REQUESTED
            BOOL bSubmit,
            BOOL bDeleteAfterSubmit)
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // Create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
      SPropValue spvProps[NUM_PROPS] = {0};
      spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag          = PR_MESSAGE_CLASS_W;
      spvProps[p_PR_ICON_INDEX].ulPropTag                 = PR_ICON_INDEX;
      spvProps[p_PR_SUBJECT_W].ulPropTag                = PR_SUBJECT_W;
      spvProps[p_PR_CONVERSATION_TOPIC_W].ulPropTag     = PR_CONVERSATION_TOPIC_W;
      spvProps[p_PR_BODY_W].ulPropTag                   = PR_BODY_W;
      spvProps[p_PR_IMPORTANCE].ulPropTag               = PR_IMPORTANCE;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].ulPropTag   = PR_READ_RECEIPT_REQUESTED;
      spvProps[p_PR_MESSAGE_FLAGS].ulPropTag             = PR_MESSAGE_FLAGS;
      spvProps[p_PR_MSG_EDITOR_FORMAT].ulPropTag         = PR_MSG_EDITOR_FORMAT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].ulPropTag         = PR_MESSAGE_LOCALE_ID;
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].ulPropTag = PR_INETMAIL_OVERRIDE_FORMAT;
      spvProps[p_PR_DELETE_AFTER_SUBMIT].ulPropTag      = PR_DELETE_AFTER_SUBMIT;
      spvProps[p_PR_INTERNET_CPID].ulPropTag            = PR_INTERNET_CPID;
      spvProps[p_PR_CONVERSATION_INDEX].ulPropTag         = PR_CONVERSATION_INDEX;
      spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Note";
      spvProps[p_PR_ICON_INDEX].Value.l = 0x103; // Unsent Mail
      spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
      spvProps[p_PR_CONVERSATION_TOPIC_W].Value.lpszW = szSubject;
      spvProps[p_PR_BODY_W].Value.lpszW = szBody;
      spvProps[p_PR_IMPORTANCE].Value.l = bHighImportance?IMPORTANCE_HIGH:IMPORTANCE_NORMAL;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].Value.b = bReadReceipt?true:false;
      spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_UNSENT;
      spvProps[p_PR_MSG_EDITOR_FORMAT].Value.l = EDITOR_FORMAT_PLAINTEXT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].Value.l = 1033; // (en-us)
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].Value.l = NULL; // Mail system chooses default encoding scheme
      spvProps[p_PR_DELETE_AFTER_SUBMIT].Value.b = bDeleteAfterSubmit?true:false;
      spvProps[p_PR_INTERNET_CPID].Value.l = cpidASCII;
      hRes = BuildConversationIndex(
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
      if (SUCCEEDED(hRes))
      {
         hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = AddRecipient(lpMAPISession,
               lpMessage,
               MAPI_TO,
               szRecipientName);
            AddInLog(true,L"CallMenu: AddRecipient - returned hRes = 0x%08X\n",hRes);
            if (SUCCEEDED(hRes))
            {
               if (bReadReceipt)
               {
                  hRes = AddReportTag(lpMessage);
               }
               if (SUCCEEDED(hRes))
               {
                  hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE);
                  if (SUCCEEDED(hRes) && bSubmit)
                  {
                     hRes = lpMessage->SubmitMessage(NULL);
                  }
               }
            }
         }
      }
      if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
         delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}
```

## <a name="see-also"></a><span data-ttu-id="12f85-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12f85-132">See also</span></span>

- [<span data-ttu-id="12f85-133">Verwenden von MAPI zum Erstellen von Outlook 2007-Elementen</span><span class="sxs-lookup"><span data-stu-id="12f85-133">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

