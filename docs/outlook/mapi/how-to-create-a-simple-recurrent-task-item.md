---
title: Erstellen eines einfachen wiederkehrenden Aufgabenelements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: be765915b729824b8c8b4209f125f354b02bad2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345472"
---
# <a name="create-a-simple-recurrent-task-item"></a>Erstellen eines einfachen wiederkehrenden Aufgabenelements

**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI kann zum Erstellen von Aufgabenelementen verwendet werden. In diesem Thema wird beschrieben, wie Sie ein einfaches wiederkehrendes Aufgabenelement erstellen.
  
Informationen zum herunterladen, anzeigen und Ausführen des Codes aus dem MFCMAPI-Anwendungs-und CreateOutlookItemsAddin-Projekt, auf das in diesem Thema verwiesen wird, finden Sie unter [install the Samples used in this section](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-create-a-task-item"></a>So erstellen Sie ein Aufgabenelement

1. Öffnen Sie einen Nachrichtenspeicher. Informationen zum Öffnen eines Nachrichtenspeichers finden Sie unter [Öffnen eines Nachrichtenspeichers](opening-a-message-store.md).
    
2. Öffnen Sie den Ordner Aufgaben im Nachrichtenspeicher. Weitere Informationen finden Sie unter **PR_IPM_TASK_ENTRYID** ([pidtagipmtaskentryid (](pidtagipmtaskentryid-canonical-property.md)).
    
3. Rufen Sie die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode im Ordner Tasks auf, um das neue Aufgabenelement zu erstellen. 
    
4. Legen Sie die **dispidTaskRecur** ([pidlidtaskrecurrence (](pidlidtaskrecurrence-canonical-property.md))-Eigenschaft und andere aufgabenbezogene Eigenschaften fest, die zum Erstellen einer wiederkehrenden Aufgabe erforderlich sind.
    
5. Speichern Sie das neue Aufgabenelement.
    
Die `AddTask` Funktion in der Datei "Tasks. cpp" des CreateOutlookItemsAddin-Projekts demonstriert diese Schritte. Die `AddTask` Funktion verwendet Parameter aus dem Dialogfeld **Aufgabe hinzufügen** , das angezeigt wird, wenn Sie im Menü **AddIns** in der MfcMapi-Beispielanwendung auf **Aufgabe hinzufügen** klicken. Die `DisplayAddTaskDialog` Funktion in Tasks. cpp zeigt das Dialogfeld an und übergibt Werte aus dem Dialogfeld an `AddTask` die Funktion. Die `DisplayAddTaskDialog` Funktion bezieht sich nicht direkt auf das Erstellen eines Aufgabenelements mithilfe von MAPI, daher ist es hier nicht aufgeführt. 
  
> [!IMPORTANT]
> Der Code in der MFCMAPI-Anwendung stellt nicht sicher, dass der **Aufgaben** Ordner ausgewählt wurde, wenn Sie im Menü AddIns auf **** den Befehl **Aufgabe hinzufügen** klicken. Das Erstellen von Aufgabenelementen in einem anderen Ordner als dem Ordner " **Aufgaben** " kann zu einem undefinierten Verhalten führen. Stellen Sie sicher, dass Sie den **Aufgaben** Ordner ausgewählt haben, bevor Sie den Befehl **Aufgabe hinzufügen** in der MfcMapi-Anwendung verwenden. 
  
Die `AddTask` Funktion wird nachfolgend aufgeführt. Beachten Sie, dass der _lpFolder_ -Parameter `AddTask` , der an die Funktion übergeben wird, ein Zeiger auf eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle ist, die den Ordner darstellt, in dem die neue Aufgabe erstellt wird. Bei der _lpFolder_ , die eine **IMAPIFolder** -Schnittstelle darstellt, ruft der Code die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode auf. Die **CreateMessage** -Methode gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine **IMessage** -Schnittstelle zurück. Der größte `AddTask` Funktionscode behandelt die Arbeit zum Angeben von Eigenschaften, die für das Aufrufen der [IMAPIProp:: SetProps](imapiprop-setprops.md) -Methode vorbereitet werden. Wenn der Aufruf der setProps-Methode erfolgreich ist, wird die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen, um die Änderungen an den Speicher zu übergeben und ein neues Aufgabenelement zu erstellen. **** 
  
Die `AddTask` -Funktion legt eine Reihe von benannten Eigenschaften fest. Informationen zu benannten Eigenschaften und deren Erstellung finden Sie unter [using MAPI to create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx). Da die für Aufgabenelemente verwendeten benannten Eigenschaften mehrere Eigenschaftssätze belegen, muss beim Erstellen von Parametern, die an die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode übergeben werden, darauf geachtet werden. 
  
Die `AddTask` Funktion verwendet die `BuildWeeklyTaskRecurrencePattern` Hilfsfunktion zum Erstellen einer Struktur, die eine Aufgabenserie zum Festlegen der **dispidTaskRecur** -Eigenschaft darstellt. Informationen zur Aufgabenserien Struktur, die die `BuildWeeklyTaskRecurrencePattern` Funktion erstellt, finden Sie unter [kanonische pidlidtaskrecurrence (-Eigenschaft](pidlidtaskrecurrence-canonical-property.md) und [pidlidrecurrencepattern (-kanonische Eigenschaft](pidlidrecurrencepattern-canonical-property.md). 

Beachten Sie, dass eine Vielzahl von Serien Mustern möglich ist, `BuildWeeklyTaskRecurrencePattern` aber die Funktion erstellt nur ein wöchentliches Serienmuster. Sie ist auch für eine Reihe von Annahmen fest codiert, beispielsweise für den Kalendertyp (Gregorianische), den ersten Tag der Woche (Sonntag) und die Anzahl der geänderten oder gelöschten Instanzen (None). Eine allgemeinere Funktion zum Erstellen von Serien Mustern muss diese Art von Variablen als Parameter akzeptieren. 
  
Nachfolgend finden Sie eine vollständige Liste `AddTask` der Funktionen. 
  
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

