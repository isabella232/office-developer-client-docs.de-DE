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
  
MAPI kann verwendet werden, um eine Nachricht zu erstellen und zu senden, die eine Lesebestätigung anfordert. Wenn eine Lesebestätigung angefordert wird, generiert das Messagingsystem und gibt einen Lesebericht an den Absender zurück, wenn der Empfänger die Nachricht öffnet.
  
Informationen zum herunterladen, anzeigen und Ausführen des Codes aus dem MFCMAPI-Anwendungs-und CreateOutlookItemsAddin-Projekt, auf das in diesem Thema verwiesen wird, finden Sie unter [install the Samples used in this section](how-to-install-the-samples-used-in-this-section.md).


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>So erstellen und senden Sie eine Nachricht, die eine Lesebestätigung anfordert

1. Erstellen Sie eine ausgehende Nachricht. Weitere Informationen zum Erstellen einer ausgehenden Nachricht finden Sie unter [Behandeln einer ausgehenden Nachricht](handling-an-outgoing-message.md).
    
2. Fügen Sie die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft hinzu, und legen Sie Sie auf **true**fest.
    
3. Fügen Sie die **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))-Eigenschaft hinzu.
    
4. Fügen Sie die **PR_REPORT_TAG** ([pidtagreporttag (](pidtagreporttag-canonical-property.md))-Eigenschaft hinzu.
    
5. Senden Sie die Nachricht, indem Sie die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode aufrufen. 
    
Die `AddMail` Funktion in der Mails. cpp-Quelldatei des CreateOutlookItemsAddin-Projekts demonstriert diese Schritte. Die `AddMail` Funktion verwendet Parameter aus dem Dialogfeld **e-Mail hinzufügen** , das angezeigt wird, wenn Sie im Menü AddIns **** in der MfcMapi-Beispielanwendung auf den Befehl **e-Mail hinzufügen** klicken. Die `DisplayAddMailDialog` Funktion in Mails. cpp zeigt das Dialogfeld an und übergibt die Werte aus dem Dialogfeld an `AddMail` die Funktion. Die `DisplayAddMailDialog` Funktion bezieht sich nicht direkt auf das Erstellen eines e-Mail-Elements mithilfe von MAPI, daher ist es hier nicht aufgeführt. Die `AddMail` Funktion wird nachfolgend aufgeführt. 
  
Beachten Sie, dass der _lpFolder_ -Parameter `AddMail` , der an die Methode übergeben wird, ein Zeiger auf eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle ist, die den Ordner darstellt, in dem die neue Nachricht erstellt wird. Bei Angabe des _lpFolder_ -Parameters, der eine **IMAPIFolder** -Schnittstelle darstellt, ruft der Code die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode auf. Die **CreateMessage** -Methode gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine [IMessage: IMAPIProp](imessageimapiprop.md) -Schnittstelle zurück. 

Der größte `AddMail` Funktionscode behandelt die Arbeit des Festlegens von Eigenschaften in Vorbereitung für das Aufrufen der [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode. Wenn der Aufruf der setProps-Methode erfolgreich ist, werden durch einen Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode die Änderungen an den Speicher übermittelt und ein neues e-Mail-Element erstellt. **** Auf Anforderung wird die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode aufgerufen, um die Nachricht zu senden. 
  
Die `AddMail` Funktion verwendet zwei Hilfsfunktionen zum Erstellen von Werten für die Eigenschaften **PR_CONVERSATION_INDEX** und **PR_REPORT_TAG** : die `BuildConversationIndex` und- `AddReportTag` Funktionen. Die `BuildConversationIndex` Funktion, die sich in CreateOutlookItemsAddin. cpp befindet, führt die gleiche Arbeit aus, die die integrierte MAPI- [ScCreateConversationIndex](sccreateconversationindex.md) -Funktion ausführt, wenn kein übergeordneter Unterhaltungsindex an Sie übergeben wird. Das Format des Unterhaltungsindex Puffers, den diese Funktionen generieren, ist in der [kanonischEn PidTagConversationIndex-Eigenschaft](pidtagconversationindex-canonical-property.md)dokumentiert. 

Die `AddReportTag` Funktion, die sich in Mails. cpp befindet, ruft wiederum `BuildReportTag` die-Funktion auf, um eine Struktur für die **PR_REPORT_TAG** -Eigenschaft zu erstellen. Informationen zur Struktur, die von der `BuildReportTag` Funktion erstellt wird, finden Sie unter [kanonische pidtagreporttag (-Eigenschaft](pidtagreporttag-canonical-property.md).
  
Nachfolgend finden Sie eine vollständige Liste `AddMail` der Funktionen. 
  
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

