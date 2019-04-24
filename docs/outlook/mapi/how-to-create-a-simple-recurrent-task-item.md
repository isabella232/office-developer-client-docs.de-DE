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
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="cf59b-103">Erstellen eines einfachen wiederkehrenden Aufgabenelements</span><span class="sxs-lookup"><span data-stu-id="cf59b-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="cf59b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf59b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf59b-105">MAPI kann zum Erstellen von Aufgabenelementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf59b-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="cf59b-106">In diesem Thema wird beschrieben, wie Sie ein einfaches wiederkehrendes Aufgabenelement erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf59b-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="cf59b-107">Informationen zum herunterladen, anzeigen und Ausführen des Codes aus dem MFCMAPI-Anwendungs-und CreateOutlookItemsAddin-Projekt, auf das in diesem Thema verwiesen wird, finden Sie unter [install the Samples used in this section](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="cf59b-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="cf59b-108">So erstellen Sie ein Aufgabenelement</span><span class="sxs-lookup"><span data-stu-id="cf59b-108">To create a task item</span></span>

1. <span data-ttu-id="cf59b-109">Öffnen Sie einen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="cf59b-109">Open a message store.</span></span> <span data-ttu-id="cf59b-110">Informationen zum Öffnen eines Nachrichtenspeichers finden Sie unter [Öffnen eines Nachrichtenspeichers](opening-a-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="cf59b-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="cf59b-111">Öffnen Sie den Ordner Aufgaben im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="cf59b-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="cf59b-112">Weitere Informationen finden Sie unter **PR_IPM_TASK_ENTRYID** ([pidtagipmtaskentryid (](pidtagipmtaskentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cf59b-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="cf59b-113">Rufen Sie die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode im Ordner Tasks auf, um das neue Aufgabenelement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf59b-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="cf59b-114">Legen Sie die **dispidTaskRecur** ([pidlidtaskrecurrence (](pidlidtaskrecurrence-canonical-property.md))-Eigenschaft und andere aufgabenbezogene Eigenschaften fest, die zum Erstellen einer wiederkehrenden Aufgabe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="cf59b-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="cf59b-115">Speichern Sie das neue Aufgabenelement.</span><span class="sxs-lookup"><span data-stu-id="cf59b-115">Save the new task item.</span></span>
    
<span data-ttu-id="cf59b-116">Die `AddTask` Funktion in der Datei "Tasks. cpp" des CreateOutlookItemsAddin-Projekts demonstriert diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="cf59b-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="cf59b-117">Die `AddTask` Funktion verwendet Parameter aus dem Dialogfeld **Aufgabe hinzufügen** , das angezeigt wird, wenn Sie im Menü **AddIns** in der MfcMapi-Beispielanwendung auf **Aufgabe hinzufügen** klicken.</span><span class="sxs-lookup"><span data-stu-id="cf59b-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="cf59b-118">Die `DisplayAddTaskDialog` Funktion in Tasks. cpp zeigt das Dialogfeld an und übergibt Werte aus dem Dialogfeld an `AddTask` die Funktion.</span><span class="sxs-lookup"><span data-stu-id="cf59b-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="cf59b-119">Die `DisplayAddTaskDialog` Funktion bezieht sich nicht direkt auf das Erstellen eines Aufgabenelements mithilfe von MAPI, daher ist es hier nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf59b-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="cf59b-120">Der Code in der MFCMAPI-Anwendung stellt nicht sicher, dass der **Aufgaben** Ordner ausgewählt wurde, wenn Sie im Menü AddIns auf \*\*\*\* den Befehl **Aufgabe hinzufügen** klicken.</span><span class="sxs-lookup"><span data-stu-id="cf59b-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="cf59b-121">Das Erstellen von Aufgabenelementen in einem anderen Ordner als dem Ordner " **Aufgaben** " kann zu einem undefinierten Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="cf59b-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="cf59b-122">Stellen Sie sicher, dass Sie den **Aufgaben** Ordner ausgewählt haben, bevor Sie den Befehl **Aufgabe hinzufügen** in der MfcMapi-Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf59b-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="cf59b-123">Die `AddTask` Funktion wird nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf59b-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="cf59b-124">Beachten Sie, dass der _lpFolder_ -Parameter `AddTask` , der an die Funktion übergeben wird, ein Zeiger auf eine [IMAPIFolder](imapifolderimapicontainer.md) -Schnittstelle ist, die den Ordner darstellt, in dem die neue Aufgabe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf59b-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="cf59b-125">Bei der _lpFolder_ , die eine **IMAPIFolder** -Schnittstelle darstellt, ruft der Code die [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="cf59b-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="cf59b-126">Die **CreateMessage** -Methode gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine **IMessage** -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="cf59b-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="cf59b-127">Der größte `AddTask` Funktionscode behandelt die Arbeit zum Angeben von Eigenschaften, die für das Aufrufen der [IMAPIProp:: SetProps](imapiprop-setprops.md) -Methode vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="cf59b-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="cf59b-128">Wenn der Aufruf der setProps-Methode erfolgreich ist, wird die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen, um die Änderungen an den Speicher zu übergeben und ein neues Aufgabenelement zu erstellen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cf59b-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="cf59b-129">Die `AddTask` -Funktion legt eine Reihe von benannten Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="cf59b-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="cf59b-130">Informationen zu benannten Eigenschaften und deren Erstellung finden Sie unter [using MAPI to create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf59b-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="cf59b-131">Da die für Aufgabenelemente verwendeten benannten Eigenschaften mehrere Eigenschaftssätze belegen, muss beim Erstellen von Parametern, die an die [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) -Methode übergeben werden, darauf geachtet werden.</span><span class="sxs-lookup"><span data-stu-id="cf59b-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="cf59b-132">Die `AddTask` Funktion verwendet die `BuildWeeklyTaskRecurrencePattern` Hilfsfunktion zum Erstellen einer Struktur, die eine Aufgabenserie zum Festlegen der **dispidTaskRecur** -Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="cf59b-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="cf59b-133">Informationen zur Aufgabenserien Struktur, die die `BuildWeeklyTaskRecurrencePattern` Funktion erstellt, finden Sie unter [kanonische pidlidtaskrecurrence (-Eigenschaft](pidlidtaskrecurrence-canonical-property.md) und [pidlidrecurrencepattern (-kanonische Eigenschaft](pidlidrecurrencepattern-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="cf59b-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="cf59b-134">Beachten Sie, dass eine Vielzahl von Serien Mustern möglich ist, `BuildWeeklyTaskRecurrencePattern` aber die Funktion erstellt nur ein wöchentliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="cf59b-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="cf59b-135">Sie ist auch für eine Reihe von Annahmen fest codiert, beispielsweise für den Kalendertyp (Gregorianische), den ersten Tag der Woche (Sonntag) und die Anzahl der geänderten oder gelöschten Instanzen (None).</span><span class="sxs-lookup"><span data-stu-id="cf59b-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="cf59b-136">Eine allgemeinere Funktion zum Erstellen von Serien Mustern muss diese Art von Variablen als Parameter akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="cf59b-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="cf59b-137">Nachfolgend finden Sie eine vollständige Liste `AddTask` der Funktionen.</span><span class="sxs-lookup"><span data-stu-id="cf59b-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="cf59b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf59b-138">See also</span></span>

- [<span data-ttu-id="cf59b-139">Verwenden von MAPI zum Erstellen von Outlook 2007-Elementen</span><span class="sxs-lookup"><span data-stu-id="cf59b-139">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

