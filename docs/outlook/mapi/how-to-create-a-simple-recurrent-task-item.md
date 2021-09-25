---
title: Erstellen eines einfachen wiederkehrenden Aufgabenelements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 09db0785b8a5d7a895d4d284603a318c623bfcae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604922"
---
# <a name="create-a-simple-recurrent-task-item"></a>Erstellen eines einfachen wiederkehrenden Aufgabenelements

**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI kann zum Erstellen von Aufgabenelementen verwendet werden. In diesem Thema wird beschrieben, wie Sie ein einfaches wiederkehrendes Aufgabenelement erstellen.
  
Informationen zum Herunterladen, Anzeigen und Ausführen des Codes aus der MFCMAPI-Anwendung und dem CreateOutlookItemsAddin-Projekt, auf das in diesem Thema verwiesen wird, finden Sie unter [Installieren der in diesem Abschnitt verwendeten Beispiele.](how-to-install-the-samples-used-in-this-section.md)

### <a name="to-create-a-task-item"></a>So erstellen Sie ein Aufgabenelement

1. Öffnen Sie einen Nachrichtenspeicher. Informationen zum Öffnen eines Nachrichtenspeichers finden Sie unter [Öffnen einer Nachricht Store](opening-a-message-store.md).
    
2. Öffnen Sie den Ordner "Aufgaben" im Nachrichtenspeicher. Weitere Informationen finden Sie unter **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).
    
3. Rufen Sie die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) im Ordner "Tasks" auf, um das neue Aufgabenelement zu erstellen. 
    
4. Legen Sie die **Eigenschaft dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) und andere aufgabenbezogene Eigenschaften fest, die zum Erstellen eines wiederkehrenden Vorgangs erforderlich sind.
    
5. Speichern Sie das neue Aufgabenelement.
    
Die  `AddTask` Funktion in der Quelldatei Tasks.cpp des Projekts CreateOutlookItemsAddin veranschaulicht diese Schritte. Die `AddTask` Funktion verwendet Parameter aus dem Dialogfeld **"Aufgabe hinzufügen",** das angezeigt wird, wenn Sie im Menü **"Add-Ins"** in der MFCMAPI-Beispielanwendung auf **"Aufgabe hinzufügen"** klicken. Die  `DisplayAddTaskDialog` Funktion in Tasks.cpp zeigt das Dialogfeld an und übergibt Werte aus dem Dialogfeld an die  `AddTask` Funktion. Die  `DisplayAddTaskDialog` Funktion bezieht sich nicht direkt auf das Erstellen eines Aufgabenelements mithilfe der MAPI, daher wird sie hier nicht aufgeführt. 
  
> [!IMPORTANT]
> Der Code in der MFCMAPI-Anwendung stellt nicht sicher, dass der Ordner **"Aufgaben"** ausgewählt wurde, wenn Sie im Menü **"Addins"** auf den Befehl **"Aufgabe hinzufügen"** klicken. Das Erstellen von Aufgabenelementen in einem anderen Ordner als **dem** Aufgabenordner kann zu nicht definiertem Verhalten führen. Stellen Sie sicher, dass Sie den Ordner **"Aufgaben"** ausgewählt haben, bevor Sie den Befehl **"Aufgabe hinzufügen"** in der MFCMAPI-Anwendung verwenden. 
  
Die  `AddTask` Funktion ist unten aufgeführt. Beachten Sie, dass der an die Funktion übergebene  _lpFolder-Parameter_  `AddTask` ein Zeiger auf eine [IMAPIFolder-Schnittstelle](imapifolderimapicontainer.md) ist, die den Ordner darstellt, in dem die neue Aufgabe erstellt wird. Angesichts des  _lpFolder-Elements,_ das eine **IMAPIFolder-Schnittstelle** darstellt, ruft der Code die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) auf. Die **CreateMessage-Methode** gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine **IMessage-Schnittstelle** zurück. Der Großteil des `AddTask` Funktionscodes übernimmt die Arbeit beim Angeben von Eigenschaften in Vorbereitung auf den Aufruf der [IMAPIProp::SetProps-Methode.](imapiprop-setprops.md) Wenn der Aufruf der **SetProps-Methode** erfolgreich ist, wird die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) aufgerufen, um die Änderungen in den Speicher zu übernehmen und ein neues Aufgabenelement zu erstellen. 
  
Die  `AddTask` Funktion legt eine Reihe benannter Eigenschaften fest. Informationen zu benannten Eigenschaften und deren Erstellung finden Sie unter [Verwenden von MAPI zum Erstellen von Outlook 2007-Elementen.](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx) Da die benannten Eigenschaften, die für Aufgabenelemente verwendet werden, mehrere Eigenschaftensätze belegen, müssen Sie beim Erstellen von Parametern vorsichtig sein, die an die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) übergeben werden. 
  
Die  `AddTask` Funktion verwendet die  `BuildWeeklyTaskRecurrencePattern` Hilfsfunktion, um eine Struktur zu erstellen, die eine Aufgabenserie zum Festlegen der **dispidTaskRecur-Eigenschaft** darstellt. Informationen zur Aufgabenserienstruktur der `BuildWeeklyTaskRecurrencePattern` Funktionsbuilds finden Sie unter [PidLidTaskRecurrence (kanonische Eigenschaft)](pidlidtaskrecurrence-canonical-property.md) und [PidLidRecurrencePattern (kanonische Eigenschaft).](pidlidrecurrencepattern-canonical-property.md) 

Beachten Sie, dass zwar eine vielzahl von Serienmustern möglich ist, die  `BuildWeeklyTaskRecurrencePattern` Funktion aber nur ein wöchentliches Serienmuster erstellt. Es ist auch für eine Reihe von Annahmen hartcodiert, z. B. den Kalendertyp (Gregorianisch), den ersten Tag der Woche (Sonntag) und die Anzahl der geänderten oder gelöschten Instanzen (keine). Eine allgemeinere Funktion zum Erstellen von Serienmustern müsste diese Variablen als Parameter akzeptieren. 
  
Es folgt die vollständige Auflistung der  `AddTask` Funktion. 
  
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

- [Verwenden von MAPI zum Erstellen von Outlook 2007-Elementen](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

