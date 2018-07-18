---
title: Erstellen Sie eine einfache e-Mail-Element
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1bbf80c8f614fc5e69773407c7882f3df8c0c81b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791832"
---
# <a name="create-a-simple-mail-item"></a>Erstellen Sie eine einfache e-Mail-Element
  
**Betrifft**: Outlook 
  
MAPI kann verwendet werden, erstellen und Senden einer Nachricht, die eine lesebestätigung anfordert. Wenn eine lesebestätigung angefordert wird, das messaging-System generiert und Lesen-Bericht an den Absender zurückgegeben, wenn der Empfänger die Nachricht öffnet.
  
Informationen zum Herunterladen, anzeigen, und führen Sie den Code aus der Anwendung MFCMAPI (engl.) und CreateOutlookItemsAddin-Projekt verwiesen, die in diesem Thema finden Sie unter [Installieren der Beispiele in diesem Abschnitt verwendet](how-to-install-the-samples-used-in-this-section.md).


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>Erstellen und Senden einer Nachricht anfordern einer lesebestätigung

1. Erstellen Sie eine ausgehende Nachricht. Informationen dazu, wie Sie eine ausgehende Nachricht zu erstellen finden Sie unter [Behandeln von ausgehenden Nachrichten](handling-an-outgoing-message.md).
    
2. Fügen Sie die Eigenschaft **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)), und legen Sie es auf **true fest**.
    
3. Fügen Sie die Eigenschaft **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
4. Fügen Sie die Eigenschaft **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)).
    
5. Senden Sie die Nachricht, durch die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode aufrufen. 
    
Die `AddMail` Funktion in der Quelldatei Mails.cpp des Projekts CreateOutlookItemsAddin veranschaulicht diese Schritte. Die `AddMail` Funktion mit Parametern im Dialogfeld **Mail hinzufügen** , der angezeigt wird, wenn Sie den Befehl **Mail hinzufügen** die Menü **-Add-Ins** in der beispielanwendung MFCMAPI (engl.) klicken. Die `DisplayAddMailDialog` -Funktion in Mails.cpp zeigt das Dialogfeld an und übergibt die Werte aus dem Dialogfeld, um die `AddMail` Funktion. Die `DisplayAddMailDialog` Funktion bezieht sich nicht direkt auf das Erstellen eines e-Mail-Elements mithilfe von MAPI, damit sie dennoch hier nicht aufgeführt ist. Die `AddMail` Funktion ist unten aufgeführt. 
  
Der _LpFolder_ -Parameter übergeben, um die `AddMail` -Methode ist ein Zeiger auf eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle, die den Ordner darstellt, in dem die neue Nachricht erstellt werden. Wenn den _LpFolder_ -Parameter, der eine Schnittstelle **IMAPIFolder** darstellt, ruft der Code die [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode. Die **CreateMessage** -Methode gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine [IMessage: IMAPIProp](imessageimapiprop.md) Schnittstelle. 

Die meisten der `AddMail` Funktionscodes übernimmt die Aufgabe Festlegen von Eigenschaften im Rahmen der Vorbereitung für die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode aufrufen. Wenn der Aufruf der **SetProps** -Methode erfolgreich ist, ein Anruf an die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode übernimmt die Änderungen an den Speicher und erstellt ein neue e-Mail-Element. Klicken Sie dann, wenn angefordert, die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode aufgerufen, um die Nachricht zu senden. 
  
Die `AddMail` -Funktion verwendet zwei Hilfsfunktionen zum Erstellen der Werte für die Eigenschaften **PR_CONVERSATION_INDEX** und **PR_REPORT_TAG** : die `BuildConversationIndex` und `AddReportTag` Funktionen. Die `BuildConversationIndex` -Funktion, befindet sich im CreateOutlookItemsAddin.cpp, funktioniert die gleichen, die die integrierte MAPI [ScCreateConversationIndex](sccreateconversationindex.md) -Funktion wird ausgeführt, wenn ein Index für übergeordnete Unterhaltung nicht an es übergeben wird. Das Format des Puffers Index Unterhaltung, die diese Funktionen generieren ist in [Kanonische-Eigenschaft PidTagConversationIndex](pidtagconversationindex-canonical-property.md)dokumentiert. 

Die `AddReportTag` -Funktion, befindet sich im Mails.cpp, ruft der `BuildReportTag` Funktion, um eine Struktur für die **PR_REPORT_TAG** -Eigenschaft erstellen. Informationen zur Struktur, die die `BuildReportTag` Builds funktioniert, finden Sie unter [PidTagReportTag kanonische-Eigenschaft](pidtagreporttag-canonical-property.md).
  
Im folgenden finden Sie eine vollständige Liste der der `AddMail` Funktion. 
  
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

- [Erstellen von Outlook 2007-Elementen mithilfe von MAPI](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

