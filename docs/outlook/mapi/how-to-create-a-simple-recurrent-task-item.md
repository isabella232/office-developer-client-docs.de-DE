---
title: Erstellen eines einfachen wiederkehrenden Aufgabe-Elements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 68d7472f993bcc35abbd4b733bae9f137b948608
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576841"
---
# <a name="create-a-simple-recurrent-task-item"></a>Erstellen eines einfachen wiederkehrenden Aufgabe-Elements

**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI kann verwendet werden, zum Erstellen von Aufgabenelementen erstellen. In diesem Thema wird das Erstellen eines einfachen wiederkehrenden Aufgabe-Elements beschrieben.
  
Informationen zum Herunterladen, anzeigen, und führen Sie den Code aus der Anwendung MFCMAPI (engl.) und CreateOutlookItemsAddin-Projekt verwiesen, die in diesem Thema finden Sie unter [Installieren der Beispiele in diesem Abschnitt verwendet](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-create-a-task-item"></a>Ein Aufgabenelement erstellen

1. Öffnen Sie einen Nachrichtenspeicher. Informationen zum Öffnen eines Nachrichtenspeichers finden Sie unter [Öffnen eines Nachrichtenspeichers](opening-a-message-store.md).
    
2. Öffnen Sie den Ordner Aufgaben im Nachrichtenspeicher. Weitere Informationen finden Sie unter **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).
    
3. Rufen Sie die [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode in den Ordner Aufgaben auf das neue Aufgabenelement erstellen. 
    
4. Legen Sie die Eigenschaft **DispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) und andere aufgabenbezogenen Eigenschaften erforderlich, um eine wiederkehrende Aufgabe erstellen.
    
5. Speichern Sie das neue Aufgabenelement.
    
Die `AddTask` Funktion in der Quelldatei Tasks.cpp des Projekts CreateOutlookItemsAddin veranschaulicht diese Schritte. Die `AddTask` Funktion mit Parametern im Dialogfeld **Aufgabe hinzufügen** , die angezeigt wird, wenn Sie die **Aufgabe hinzufügen** die Menü **-Add-Ins** in der beispielanwendung MFCMAPI (engl.) klicken. Die `DisplayAddTaskDialog` -Funktion in Tasks.cpp zeigt das Dialogfeld an und übergibt die Werte aus dem Dialogfeld, um die `AddTask` Funktion. Die `DisplayAddTaskDialog` Funktion bezieht sich nicht direkt auf das Erstellen eines Aufgabenelements mithilfe von MAPI, damit sie dennoch hier nicht aufgeführt ist. 
  
> [!IMPORTANT]
> Der Code in der Anwendung MFCMAPI (engl.) stellt nicht sicher, dass der Ordner **Aufgaben** ausgewählt wurde, wenn Sie den Befehl **Aufgabe hinzufügen** die Menü **-Add-Ins** klicken. Erstellen von Aufgabenelementen in einem anderen Ordner als dem Ordner **Aufgaben** kann nicht definiertem Verhalten führen. Stellen Sie sicher, dass Sie den Ordner **Aufgaben** ausgewählt haben, bevor Sie mit dem Befehl **Aufgabe hinzufügen** in der Anwendung MFCMAPI (engl.). 
  
Die `AddTask` Funktion ist unten aufgeführt. Der _LpFolder_ -Parameter übergeben, um die `AddTask` Funktion ist ein Zeiger auf eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle, die den Ordner darstellt, in dem die neue Aufgabe erstellt wird. Die _LpFolder_ , die eine **IMAPIFolder** -Schnittstelle stellt angegeben, ruft der Code die [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode. Die **CreateMessage** -Methode gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine **IMessage** -Schnittstelle zurück. Die meisten der `AddTask` Funktionscodes übernimmt die Aufgabe angeben von Eigenschaften in Vorbereitung auf die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode aufrufen. Wenn der Aufruf der **SetProps** -Methode erfolgreich ist, wird die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen, um einen commit der Änderungen an den Speicher und ein neues Aufgabenelement erstellen. 
  
Die `AddTask` Funktion wird eine Reihe von benannten Eigenschaften. Informationen zu benannten Eigenschaften und wie sie erstellt werden finden Sie unter [Verwenden von MAPI in Outlook 2007-Einträge erstellen](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx). Da die benannten Eigenschaften für Aufgabenelemente mehrere Eigenschaftensätze belegen, muss darauf geachtet werden beim Erstellen von Parametern an die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode übergeben. 
  
Die `AddTask` Funktion verwendet die `BuildWeeklyTaskRecurrencePattern` Hilfsfunktion erstellen Sie eine Struktur, die eine Aufgabenserie zum Festlegen der **DispidTaskRecur** -Eigenschaft darstellt. Informationen über die Aufgabe Serie Struktur der `BuildWeeklyTaskRecurrencePattern` Builds funktioniert, finden Sie unter [PidLidTaskRecurrence kanonische-Eigenschaft](pidlidtaskrecurrence-canonical-property.md) und [PidLidRecurrencePattern kanonische-Eigenschaft](pidlidrecurrencepattern-canonical-property.md). 

Beachten Sie, dass eine Vielzahl von Serienmuster möglich ist, sind die `BuildWeeklyTaskRecurrencePattern` Funktion nur ein wöchentliches Serienmuster erstellt. Es ist auch für eine Reihe von Annahmen, wie etwa den Kalendertyp (Gregorianisch), den ersten Tag der Woche (Sonntag), und die Anzahl der geänderten oder gelöschten Instanzen (kein Rahmen) codiert. Weitere allgemeine müssten Serie Muster die Funktion zum Erstellen dieser Art von Variablen als Parameter akzeptiert. 
  
Im folgenden finden Sie eine vollständige Liste der der `AddTask` Funktion. 
  
```cpp
HRESULT AddTask(LPMAPIFOLDER lpFolder,
            SYSTEMTIME* lpstStart, // PidLidCommonEnd, PidLidTaskDueDate, PidLidTaskRecurrence
            SYSTEMTIME* lpstEnd, // PidLidTaskRecurrence
            SYSTEMTIME* lpstFirstDOW, // PidLidTaskRecurrence
            DWORD dwPeriod, // PidLidTaskRecurrence
            DWORD dwOccurrenceCount, // PidLidTaskRecurrence
            DWORD dwPatternTypeSpecific, // PidLidTaskRecurrence
            LPWSTR szSubject, // PR_SUBJECT_W
            LPWSTR szBody) // PR_BODY_W
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      MAPINAMEID  rgnmid[ulTaskProps];
      LPMAPINAMEID rgpnmid[ulTaskProps];
      LPSPropTagArray lpNamedPropTags = NULL;
      ULONG i = 0;
      for (i = 0 ; i < ulTaskProps ; i++)
      {
         if (i < ulFirstTaskProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Common;
         else
            rgnmid[i].lpguid = (LPGUID)&PSETID_Task;
         rgnmid[i].ulKind = MNID_ID;
         rgnmid[i].Kind.lID = aulTaskProps[i];
         rgpnmid[i] = &rgnmid[i];
      }
      hRes = lpFolder->GetIDsFromNames(
         ulTaskProps,
         (LPMAPINAMEID*) &rgpnmid,
         NULL,
         &lpNamedPropTags);
      if (SUCCEEDED(hRes) && lpNamedPropTags)
      {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
         SPropValue spvProps[NUM_PROPS] = {0};
         spvProps[p_PidLidTaskMode].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskMode],PT_LONG);
         spvProps[p_PidLidCommonEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonEnd],PT_SYSTIME);
         spvProps[p_PidLidTaskStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskStatus],PT_LONG);
         spvProps[p_PidLidPercentComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidPercentComplete],PT_DOUBLE);
         spvProps[p_PidLidTaskState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskState],PT_LONG);
         spvProps[p_PidLidTaskRecurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskRecurrence],PT_BINARY);
         spvProps[p_PidLidTaskDeadOccurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDeadOccurrence],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwner].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwner],PT_UNICODE);
         spvProps[p_PidLidTaskFRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFRecurring],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwnership].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwnership],PT_LONG);
         spvProps[p_PidLidTaskAcceptanceState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskAcceptanceState],PT_LONG);
         spvProps[p_PidLidTaskFFixOffline].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFFixOffline],PT_BOOLEAN);
         spvProps[p_PidLidTaskDueDate].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDueDate],PT_SYSTIME);
         spvProps[p_PidLidTaskComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskComplete],PT_SYSTIME);
         spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag   = PR_MESSAGE_CLASS_W;
         spvProps[p_PR_ICON_INDEX].ulPropTag        = PR_ICON_INDEX;
         spvProps[p_PR_SUBJECT_W].ulPropTag         = PR_SUBJECT_W;
         spvProps[p_PR_MESSAGE_FLAGS].ulPropTag     = PR_MESSAGE_FLAGS;
         spvProps[p_PR_BODY_W].ulPropTag            = PR_BODY_W;
         spvProps[p_PidLidTaskMode].Value.l = tdmtNothing;
         SYSTEMTIME stStartUTC = {0};
         TzSpecificLocalTimeToSystemTime(NULL,lpstStart,&stStartUTC);
         SystemTimeToFileTime(&stStartUTC,&spvProps[p_PidLidCommonEnd].Value.ft);
         spvProps[p_PidLidTaskStatus].Value.l = tsvNotStarted;
         spvProps[p_PidLidPercentComplete].Value.dbl = 0.0;
         spvProps[p_PidLidTaskState].Value.l = tdsOWNNEW;
         spvProps[p_PidLidTaskDeadOccurrence].Value.b = false;
         spvProps[p_PidLidTaskOwner].Value.lpszW = L"Unknown";
         spvProps[p_PidLidTaskFRecurring].Value.b = true;
         spvProps[p_PidLidTaskOwnership].Value.l = tovNew;
         spvProps[p_PidLidTaskAcceptanceState].Value.l = tdvNone;
         spvProps[p_PidLidTaskFFixOffline].Value.b = true;
         SystemTimeToFileTime(lpstStart,&spvProps[p_PidLidTaskDueDate].Value.ft);
         spvProps[p_PidLidTaskComplete].Value.b = false;
         spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Task";
         spvProps[p_PR_ICON_INDEX].Value.l = 0x501; // Unassigned Recurring Task
         spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
         spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_READ;
         spvProps[p_PR_BODY_W].Value.lpszW = szBody;
         hRes = BuildWeeklyTaskRecurrencePattern(
            lpstStart,
            lpstEnd,
            lpstFirstDOW,
            dwPeriod,
            dwOccurrenceCount,
            dwPatternTypeSpecific,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.cb,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.lpb);
         if (SUCCEEDED(hRes))
         {
            hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
            if (SUCCEEDED(hRes))
            {
               hRes = lpMessage->SaveChanges(FORCE_SAVE);
            }
         }
         if (spvProps[p_PidLidTaskRecurrence].Value.bin.lpb)
            delete[] spvProps[p_PidLidTaskRecurrence].Value.bin.lpb;
      }
      MAPIFreeBuffer(lpNamedPropTags);
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}

```

## <a name="see-also"></a>Siehe auch

- [Erstellen von Outlook 2007-Elementen mithilfe von MAPI](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

