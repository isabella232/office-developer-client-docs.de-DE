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
# <a name="create-a-simple-mail-item"></a>Erstellen eines einfachen E-Mail-Elements
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI kann verwendet werden, um eine Nachricht zu erstellen und zu senden, die eine Lesebestätigung anfordert. Wenn ein Lesebeleg angefordert wird, generiert und gibt das Messagingsystem einen Lesebericht an den Absender zurück, wenn der Empfänger die Nachricht öffnet.
  
Informationen zum Herunterladen, Anzeigen und Ausführen des Codes aus der MFCMAPI-Anwendung und dem CreateOutlookItemsAddin-Projekt, auf das in diesem Thema verwiesen wird, finden Sie unter [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>So erstellen und senden Sie eine Nachricht, die eine Lesebestätigung anfordert

1. Erstellen Sie eine ausgehende Nachricht. Informationen zum Erstellen einer ausgehenden Nachricht finden Sie unter [Handling an Outgoing Message](handling-an-outgoing-message.md).
    
2. Fügen Sie **die PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) -Eigenschaft hinzu, und legen Sie sie auf **true .**
    
3. Fügen Sie **die PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) -Eigenschaft hinzu.
    
4. Fügen Sie **die PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) -Eigenschaft hinzu.
    
5. Senden Sie die Nachricht, indem Sie die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufrufen. 
    
Die  `AddMail` Funktion in der Quelldatei "Mails.cpp" des CreateOutlookItemsAddin-Projekts veranschaulicht diese Schritte. Die Funktion übernimmt Parameter aus dem Dialogfeld E-Mail hinzufügen, das angezeigt wird, wenn Sie im Menü `AddMail` **Addins** in der  MFCMAPI-Beispielanwendung auf den Befehl E-Mail hinzufügen klicken.  Die Funktion in Mails.cpp zeigt das Dialogfeld an und übergibt die Werte aus dem Dialogfeld  `DisplayAddMailDialog` an die  `AddMail` Funktion. Die Funktion bezieht sich nicht direkt auf das Erstellen eines  `DisplayAddMailDialog` E-Mail-Elements mithilfe von MAPI, daher ist sie hier nicht aufgeführt. Die  `AddMail` Funktion ist unten aufgeführt. 
  
Beachten Sie, dass der an die Methode übergebene  _lpFolder-Parameter_ ein Zeiger auf eine  `AddMail` [IMAPIFolder-Schnittstelle](imapifolderimapicontainer.md) ist, die den Ordner darstellt, in dem die neue Nachricht erstellt wird. Angesichts des  _lpFolder-Parameters,_ der eine **IMAPIFolder-Schnittstelle** darstellt, ruft der Code die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) auf. Die **CreateMessage-Methode** gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine [IMessage : IMAPIProp-Schnittstelle](imessageimapiprop.md) zurück. 

Der großteil des Funktionscodes übernimmt die Arbeit beim Festlegen von Eigenschaften in Vorbereitung auf den Aufruf der `AddMail` [IMAPIProp::SetProps-Methode.](imapiprop-setprops.md) Wenn der Aufruf der **SetProps-Methode** erfolgreich ist, werden bei einem Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) die Änderungen an den Speicher commits und ein neues E-Mail-Element erstellt. Wenn angefordert, wird dann die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufgerufen, um die Nachricht zu senden. 
  
Die Funktion verwendet zwei Hilfsfunktionen, um Werte für die Eigenschaften PR_CONVERSATION_INDEX und PR_REPORT_TAG zu `AddMail` erstellen: die   `BuildConversationIndex` `AddReportTag` und-Funktionen. Die Funktion in CreateOutlookItemsAddin.cpp führt die gleiche Arbeit aus wie die integrierte  `BuildConversationIndex` MAPI [ScCreateConversationIndex-Funktion,](sccreateconversationindex.md) wenn kein übergeordneter Unterhaltungsindex an sie übergeben wird. Das Format des Unterhaltungsindexpuffers, den diese Funktionen generieren, ist in [der kanonischen Eigenschaft PidTagConversationIndex dokumentiert.](pidtagconversationindex-canonical-property.md) 

Die In Mails.cpp enthaltene Funktion ruft wiederum die Funktion auf, um eine Struktur für die PR_REPORT_TAG `AddReportTag` `BuildReportTag` erstellen.  Informationen zur Struktur, die die Funktion erstellt, finden Sie  `BuildReportTag` unter [PidTagReportTag Canonical Property](pidtagreporttag-canonical-property.md).
  
Im Folgenden finden Sie die vollständige Auflistung der  `AddMail` Funktion. 
  
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

## <a name="see-also"></a>Siehe auch

- [Verwenden von MAPI zum Erstellen von Outlook 2007-Elementen](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

