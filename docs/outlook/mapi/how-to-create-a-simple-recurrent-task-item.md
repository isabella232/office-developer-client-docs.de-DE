---
title: Erstellen eines einfachen wiederkehrenden Aufgabe-Elements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 926b33fa3627461139362737f86248f217191534
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791843"
---
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="c2e70-103">Erstellen eines einfachen wiederkehrenden Aufgabe-Elements</span><span class="sxs-lookup"><span data-stu-id="c2e70-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="c2e70-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2e70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2e70-105">MAPI kann verwendet werden, zum Erstellen von Aufgabenelementen erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2e70-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="c2e70-106">In diesem Thema wird das Erstellen eines einfachen wiederkehrenden Aufgabe-Elements beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c2e70-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="c2e70-107">Informationen zum Herunterladen, anzeigen, und führen Sie den Code aus der Anwendung MFCMAPI (engl.) und CreateOutlookItemsAddin-Projekt verwiesen, die in diesem Thema finden Sie unter [Installieren der Beispiele in diesem Abschnitt verwendet](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="c2e70-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="c2e70-108">Ein Aufgabenelement erstellen</span><span class="sxs-lookup"><span data-stu-id="c2e70-108">To create a task item</span></span>

1. <span data-ttu-id="c2e70-109">Öffnen Sie einen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="c2e70-109">Open a message store.</span></span> <span data-ttu-id="c2e70-110">Informationen zum Öffnen eines Nachrichtenspeichers finden Sie unter [Öffnen eines Nachrichtenspeichers](opening-a-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="c2e70-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="c2e70-111">Öffnen Sie den Ordner Aufgaben im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="c2e70-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="c2e70-112">Weitere Informationen finden Sie unter **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c2e70-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="c2e70-113">Rufen Sie die [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode in den Ordner Aufgaben auf das neue Aufgabenelement erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2e70-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="c2e70-114">Legen Sie die Eigenschaft **DispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) und andere aufgabenbezogenen Eigenschaften erforderlich, um eine wiederkehrende Aufgabe erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2e70-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="c2e70-115">Speichern Sie das neue Aufgabenelement.</span><span class="sxs-lookup"><span data-stu-id="c2e70-115">Save the new task item.</span></span>
    
<span data-ttu-id="c2e70-116">Die `AddTask` Funktion in der Quelldatei Tasks.cpp des Projekts CreateOutlookItemsAddin veranschaulicht diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="c2e70-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="c2e70-117">Die `AddTask` Funktion mit Parametern im Dialogfeld **Aufgabe hinzufügen** , die angezeigt wird, wenn Sie die **Aufgabe hinzufügen** die Menü **-Add-Ins** in der beispielanwendung MFCMAPI (engl.) klicken.</span><span class="sxs-lookup"><span data-stu-id="c2e70-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="c2e70-118">Die `DisplayAddTaskDialog` -Funktion in Tasks.cpp zeigt das Dialogfeld an und übergibt die Werte aus dem Dialogfeld, um die `AddTask` Funktion.</span><span class="sxs-lookup"><span data-stu-id="c2e70-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="c2e70-119">Die `DisplayAddTaskDialog` Funktion bezieht sich nicht direkt auf das Erstellen eines Aufgabenelements mithilfe von MAPI, damit sie dennoch hier nicht aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="c2e70-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="c2e70-120">Der Code in der Anwendung MFCMAPI (engl.) stellt nicht sicher, dass der Ordner **Aufgaben** ausgewählt wurde, wenn Sie den Befehl **Aufgabe hinzufügen** die Menü **-Add-Ins** klicken.</span><span class="sxs-lookup"><span data-stu-id="c2e70-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="c2e70-121">Erstellen von Aufgabenelementen in einem anderen Ordner als dem Ordner **Aufgaben** kann nicht definiertem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="c2e70-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="c2e70-122">Stellen Sie sicher, dass Sie den Ordner **Aufgaben** ausgewählt haben, bevor Sie mit dem Befehl **Aufgabe hinzufügen** in der Anwendung MFCMAPI (engl.).</span><span class="sxs-lookup"><span data-stu-id="c2e70-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="c2e70-123">Die `AddTask` Funktion ist unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2e70-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="c2e70-124">Der _LpFolder_ -Parameter übergeben, um die `AddTask` Funktion ist ein Zeiger auf eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle, die den Ordner darstellt, in dem die neue Aufgabe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c2e70-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="c2e70-125">Die _LpFolder_ , die eine **IMAPIFolder** -Schnittstelle stellt angegeben, ruft der Code die [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c2e70-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="c2e70-126">Die **CreateMessage** -Methode gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine **IMessage** -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="c2e70-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="c2e70-127">Die meisten der `AddTask` Funktionscodes übernimmt die Aufgabe angeben von Eigenschaften in Vorbereitung auf die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c2e70-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="c2e70-128">Wenn der Aufruf der **SetProps** -Methode erfolgreich ist, wird die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen, um einen commit der Änderungen an den Speicher und ein neues Aufgabenelement erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2e70-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="c2e70-129">Die `AddTask` Funktion wird eine Reihe von benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2e70-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="c2e70-130">Informationen zu benannten Eigenschaften und wie sie erstellt werden finden Sie unter [Verwenden von MAPI in Outlook 2007-Einträge erstellen](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2e70-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="c2e70-131">Da die benannten Eigenschaften für Aufgabenelemente mehrere Eigenschaftensätze belegen, muss darauf geachtet werden beim Erstellen von Parametern an die [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="c2e70-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="c2e70-132">Die `AddTask` Funktion verwendet die `BuildWeeklyTaskRecurrencePattern` Hilfsfunktion erstellen Sie eine Struktur, die eine Aufgabenserie zum Festlegen der **DispidTaskRecur** -Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2e70-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="c2e70-133">Informationen über die Aufgabe Serie Struktur der `BuildWeeklyTaskRecurrencePattern` Builds funktioniert, finden Sie unter [PidLidTaskRecurrence kanonische-Eigenschaft](pidlidtaskrecurrence-canonical-property.md) und [PidLidRecurrencePattern kanonische-Eigenschaft](pidlidrecurrencepattern-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="c2e70-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="c2e70-134">Beachten Sie, dass eine Vielzahl von Serienmuster möglich ist, sind die `BuildWeeklyTaskRecurrencePattern` Funktion nur ein wöchentliches Serienmuster erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2e70-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="c2e70-135">Es ist auch für eine Reihe von Annahmen, wie etwa den Kalendertyp (Gregorianisch), den ersten Tag der Woche (Sonntag), und die Anzahl der geänderten oder gelöschten Instanzen (kein Rahmen) codiert.</span><span class="sxs-lookup"><span data-stu-id="c2e70-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="c2e70-136">Weitere allgemeine müssten Serie Muster die Funktion zum Erstellen dieser Art von Variablen als Parameter akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c2e70-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="c2e70-137">Im folgenden finden Sie eine vollständige Liste der der `AddTask` Funktion.</span><span class="sxs-lookup"><span data-stu-id="c2e70-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="c2e70-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2e70-138">See also</span></span>

- [<span data-ttu-id="c2e70-139">Erstellen von Outlook 2007-Elementen mithilfe von MAPI</span><span class="sxs-lookup"><span data-stu-id="c2e70-139">Using MAPI to Create Outlook 2007 Items</span></span>](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

