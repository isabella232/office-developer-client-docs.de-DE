---
title: Erstellen eines komplexen Terminserienelements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da9626da-5ba5-4f18-954c-4e23971d23e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d44bf5cccd7e846530eae0c03b8d3ff525f3c012
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344534"
---
# <a name="create-a-complex-recurrent-appointment-item"></a><span data-ttu-id="76f63-103">Erstellen eines komplexen Terminserienelements</span><span class="sxs-lookup"><span data-stu-id="76f63-103">Create a complex recurrent appointment item</span></span>
  
<span data-ttu-id="76f63-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76f63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76f63-105">MAPI kann verwendet werden, um Terminserienelemente zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76f63-105">MAPI can be used to create recurring appointment items.</span></span>
  
<span data-ttu-id="76f63-106">Informationen zum Herunterladen, Anzeigen und Ausführen des Codes aus der MFCMAPI-Anwendung und dem CreateOutlookItemsAddin-Projekt, auf das in diesem Thema verwiesen wird, finden Sie unter [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="76f63-106">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-an-appointment-item"></a><span data-ttu-id="76f63-107">So erstellen Sie ein Terminelement</span><span class="sxs-lookup"><span data-stu-id="76f63-107">To create an appointment item</span></span>

1. <span data-ttu-id="76f63-108">Öffnen Sie einen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="76f63-108">Open a message store.</span></span> <span data-ttu-id="76f63-109">Informationen zum Öffnen eines Nachrichtenspeichers finden Sie unter [Opening a Message Store](opening-a-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="76f63-109">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="76f63-110">Öffnen Sie einen Kalenderordner im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="76f63-110">Open a Calendar folder in the message store.</span></span> <span data-ttu-id="76f63-111">Siehe **PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="76f63-111">See **PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="76f63-112">Rufen Sie [die IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) im Ordner Kalender auf, um das neue Terminelement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76f63-112">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Calendar folder to create the new appointment item.</span></span> 
    
4. <span data-ttu-id="76f63-113">Legen Sie **die dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md))-Eigenschaft und andere Eigenschaften, die zum Erstellen eines Terminserientermins erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="76f63-113">Set the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property and other properties required to create a recurrent appointment.</span></span>
    
5. <span data-ttu-id="76f63-114">Speichern Sie das neue Terminelement.</span><span class="sxs-lookup"><span data-stu-id="76f63-114">Save the new appointment item.</span></span>
    
<span data-ttu-id="76f63-115">Die  `AddAppointment` Funktion in der Appointments.cpp-Quelldatei des CreateOutlookItemsAddin-Projekts veranschaulicht diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="76f63-115">The  `AddAppointment` function in the Appointments.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="76f63-116">Die Funktion übernimmt Parameter aus dem Dialogfeld Termin hinzufügen, das angezeigt wird, wenn Sie im Menü `AddAppointment` **Addins** in der  MFCMAPI-Beispielanwendung auf Termin hinzufügen klicken. </span><span class="sxs-lookup"><span data-stu-id="76f63-116">The  `AddAppointment` function takes parameters from the **Add Appointment** dialog box that is displayed when you click **Add Appointment** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="76f63-117">Die Funktion in Appointments.cpp zeigt das Dialogfeld an und übergibt Werte aus dem Dialogfeld  `DisplayAddAppointmentDialog` an die  `AddAppointment` Funktion.</span><span class="sxs-lookup"><span data-stu-id="76f63-117">The  `DisplayAddAppointmentDialog` function in Appointments.cpp displays the dialog box and passes values from the dialog box to the  `AddAppointment` function.</span></span> <span data-ttu-id="76f63-118">Die Funktion bezieht sich nicht direkt auf das Erstellen eines  `DisplayAddAppointmentDialog` Terminelements mithilfe von MAPI, daher ist sie hier nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="76f63-118">The  `DisplayAddAppointmentDialog` function does not relate directly to creating an appointment item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="76f63-119">Der Code in der MFCMAPI-Anwendung  stellt nicht sicher, dass  der Ordner Kalender ausgewählt wurde, wenn Sie im Menü **Addins** auf den Befehl Termin hinzufügen klicken.</span><span class="sxs-lookup"><span data-stu-id="76f63-119">The code in the MFCMAPI application does not ensure that the **Calendar** folder has been selected when you click the **Add Appointment** command on the **Addins** menu.</span></span> <span data-ttu-id="76f63-120">Das Erstellen eines Terminelements in einem anderen Ordner als dem **Kalenderordner** kann zu einem nicht definierten Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="76f63-120">Creating an appointment item in a folder other than the **Calendar** folder can cause undefined behavior.</span></span> <span data-ttu-id="76f63-121">Stellen Sie sicher, dass Sie den Ordner **Kalender ausgewählt** haben, bevor Sie den Befehl **Termin** hinzufügen in der MFCMAPI-Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="76f63-121">Make sure that you have selected the **Calendar** folder before using the **Add Appointment** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="76f63-122">Die  `AddAppointment` Methode ist unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="76f63-122">The  `AddAppointment` method is listed below.</span></span> <span data-ttu-id="76f63-123">Beachten Sie, dass der an die Methode übergebene  _lpFolder-Parameter_ ein Zeiger auf eine  `AddAppointment` [IMAPIFolder-Schnittstelle](imapifolderimapicontainer.md) ist, die den Ordner darstellt, in dem der Terminserientermin erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="76f63-123">Note that the  _lpFolder_ parameter passed to the  `AddAppointment` method is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the recurrent appointment is created.</span></span> <span data-ttu-id="76f63-124">Angesichts des  _lpFolder-Parameters,_ der eine **IMAPIFolder-Schnittstelle** darstellt, ruft der Code die [IMAPIFolder::CreateMessage-Methode](imapifolder-createmessage.md) auf.</span><span class="sxs-lookup"><span data-stu-id="76f63-124">Given the  _lpFolder_ parameter that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="76f63-125">Die **CreateMessage-Methode** gibt einen Erfolgscode und einen Zeiger auf einen Zeiger auf eine **IMessage-Schnittstelle** zurück.</span><span class="sxs-lookup"><span data-stu-id="76f63-125">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="76f63-126">Der Großteil des Funktionscodes übernimmt das Angeben von Eigenschaften in Vorbereitung auf den Aufruf der `AddAppointment` [IMAPIProp::SetProps-Methode.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="76f63-126">Most of the  `AddAppointment` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="76f63-127">Wenn der Aufruf der **SetProps-Methode** erfolgreich ist, wird die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) aufgerufen, um die Änderungen an den Speicher zu commiten und ein neues Kalenderelement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76f63-127">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new calendar item.</span></span> 
  
<span data-ttu-id="76f63-128">Die  `AddAppointment` Funktion legt eine Reihe benannter Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="76f63-128">The  `AddAppointment` function sets a number of named properties.</span></span> <span data-ttu-id="76f63-129">Informationen zu benannten Eigenschaften und deren Erstellung finden Sie unter [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="76f63-129">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="76f63-130">Da die benannten Eigenschaften, die für Terminelemente verwendet werden, mehrere Eigenschaftssätze belegen, müssen Sie beim Erstellen von Parametern darauf achten, dass sie an die [IMAPIProp::GetIDsFromNames-Methode übergeben](imapiprop-getidsfromnames.md) werden.</span><span class="sxs-lookup"><span data-stu-id="76f63-130">Because the named properties used for appointment items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="76f63-131">Die  `AddAppointment` Funktion verwendet mehrere Hilfsfunktionen, um eine Struktur für verschiedene terminbezogene Eigenschaften zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76f63-131">The  `AddAppointment` function uses several helper functions to build a structure for various appointment-related properties.</span></span> <span data-ttu-id="76f63-132">Die  `BuildTimeZoneStruct` Funktionen  `BuildTimeZoneDefinition` und Hilfsfunktionen werden verwendet, um eine Struktur zu erstellen, die die zeitzonenbezogenen Eigenschaften angibt.</span><span class="sxs-lookup"><span data-stu-id="76f63-132">The  `BuildTimeZoneStruct` and  `BuildTimeZoneDefinition` helper functions are used to build a structure that specifies the time-zone-related properties.</span></span> <span data-ttu-id="76f63-133">Die zeitzonenbezogenen Eigenschaften sind **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), **dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md)), **dispidApptTZDefRecur** ([PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md)), **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) und **dispidApptTZDefEndDisplay** ([PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)), und sie werden in den entsprechenden Abschnitten von [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx)erläutert.</span><span class="sxs-lookup"><span data-stu-id="76f63-133">The time-zone-related properties are **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)), **dispidTimeZoneDesc** ([PidLidTimeZoneDescription](pidlidtimezonedescription-canonical-property.md)), **dispidApptTZDefRecur** ([PidLidAppointmentTimeZoneDefinitionRecur](pidlidappointmenttimezonedefinitionrecur-canonical-property.md)), **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)), and **dispidApptTZDefEndDisplay** ([PidLidAppointmentTimeZoneDefinitionEndDisplay](pidlidappointmenttimezonedefinitionenddisplay-canonical-property.md)), and they are discussed in the corresponding sections of [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx).</span></span> 

<span data-ttu-id="76f63-134">Die Funktion wird verwendet, um eine Struktur zu erstellen, die die  `BuildGlobalObjectID` **Eigenschaften LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) und **dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) angibt, die in den entsprechenden Abschnitten von [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx)behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="76f63-134">The  `BuildGlobalObjectID` function is used to build a structure that specifies the **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) and **dispidCleanGlobalObjId** ([PidLidCleanGlobalObjectId](pidlidcleanglobalobjectid-canonical-property.md)) properties, which are discussed in the corresponding sections of [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28v=EXCHG.80%29.aspx).</span></span> <span data-ttu-id="76f63-135">Die Struktur, die die **dispidApptRecur-Eigenschaft angibt,** wird mithilfe der Funktion  `BuildWeeklyAppointmentRecurrencePattern` erstellt.</span><span class="sxs-lookup"><span data-stu-id="76f63-135">The structure that specifies the **dispidApptRecur** property is built using the  `BuildWeeklyAppointmentRecurrencePattern` function.</span></span> 

<span data-ttu-id="76f63-136">Informationen zur struktur, die von der Funktion erstellt wird, finden Sie  `BuildWeeklyAppointmentRecurrencePattern` unter [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="76f63-136">For information about the structure built by the  `BuildWeeklyAppointmentRecurrencePattern` function, see [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span></span> <span data-ttu-id="76f63-137">Beachten Sie, dass zwar eine vielzahl von Terminserienmustern möglich ist, die Funktion jedoch nur ein wöchentliches  `BuildWeeklyAppointmentRecurrencePattern` Terminserienmuster erstellt.</span><span class="sxs-lookup"><span data-stu-id="76f63-137">Note that while a large variety of appointment recurrence patterns are possible, the  `BuildWeeklyAppointmentRecurrencePattern` function only builds a weekly appointment recurrence pattern.</span></span> <span data-ttu-id="76f63-138">Außerdem werden mehrere hart codierte Werte verwendet, z. B. der Kalendertyp (Gregorianisch), der erste Wochentag (Sonntag) und die Anzahl der geänderten oder gelöschten Instanzen (keine).</span><span class="sxs-lookup"><span data-stu-id="76f63-138">It also uses several hard-coded values, such as the calendar type (Gregorian), the first day of the week (Sunday), and number of modified or deleted instances (none).</span></span> <span data-ttu-id="76f63-139">Eine allgemeinere Funktion zum Erstellen von Terminserienmustern müsste diese Arten von Variablen als Parameter akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="76f63-139">A more general purpose appointment recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="76f63-140">Im Folgenden finden Sie die vollständige Auflistung der  `AddAppointment` Funktion.</span><span class="sxs-lookup"><span data-stu-id="76f63-140">The following is the complete listing of the  `AddAppointment` function.</span></span> 
  
```cpp
HRESULT AddAppointment(LPMAPIFOLDER lpFolder,
               SYSTEMTIME* lpstStartDateLocal, // PidLidAppointmentRecur
               SYSTEMTIME* lpstEndDateLocal, // PidLidAppointmentRecur
               SYSTEMTIME* lpstStartFirstUST, // PidLidAppointmentStartWhole, PidLidCommonStart, PR_START_DATE
               SYSTEMTIME* lpstEndFirstUST, // PidLidAppointmentEndWhole, PidLidCommonEnd, PR_END_DATE
               SYSTEMTIME* lpszClipStartUST, // PidLidClipStart
               SYSTEMTIME* lpstClipEndUST, // PidLidClipEnd
               SYSTEMTIME* lpstFirstDOW, // PidLidAppointmentRecur
               DWORD dwStartOffsetLocal, // PidLidAppointmentRecur
               DWORD dwEndOffsetLocal, // PidLidAppointmentRecur
               DWORD dwPeriod, // PidLidAppointmentRecur
               DWORD dwOccurrenceCount, // PidLidAppointmentRecur
               DWORD dwPatternTypeSpecific, // PidLidAppointmentRecur
               ULONG ulDuration, // PidLidAppointmentDuration
               LPWSTR szSubject, // PR_SUBJECT_W
               LPWSTR szLocation, // PidLidLocation
               LPWSTR szPattern) // PidLidRecurrencePattern
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
      MAPINAMEID  rgnmid[ulAppointmentProps];
      LPMAPINAMEID rgpnmid[ulAppointmentProps];
      LPSPropTagArray lpNamedPropTags = NULL;
      ULONG i = 0;
      for (i = 0 ; i < ulAppointmentProps ; i++)
      {
         if (i < ulFirstMeetingProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Appointment;
         else if (i < ulFirstCommonProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Meeting;
         else
            rgnmid[i].lpguid = (LPGUID)&PSETID_Common;
         rgnmid[i].ulKind = MNID_ID;
         rgnmid[i].Kind.lID = aulAppointmentProps[i];
         rgpnmid[i] = &rgnmid[i];
      }
      hRes = lpFolder->GetIDsFromNames(
         ulAppointmentProps,
         (LPMAPINAMEID*) &rgpnmid,
         NULL,
         &lpNamedPropTags);
      if (SUCCEEDED(hRes) && lpNamedPropTags)
      {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
         SPropValue spvProps[NUM_PROPS] = {0};
         spvProps[p_PidLidAppointmentSequence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentSequence],PT_LONG);
         spvProps[p_PidLidBusyStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidBusyStatus],PT_LONG);
         spvProps[p_PidLidLocation].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidLocation],PT_UNICODE);
         spvProps[p_PidLidAppointmentStartWhole].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentStartWhole],PT_SYSTIME);
         spvProps[p_PidLidAppointmentEndWhole].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentEndWhole],PT_SYSTIME);
         spvProps[p_PidLidAppointmentDuration].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentDuration],PT_LONG);
         spvProps[p_PidLidAppointmentColor].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentColor],PT_LONG);
         spvProps[p_PidLidResponseStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidResponseStatus],PT_LONG);
         spvProps[p_PidLidRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurring],PT_BOOLEAN);
         spvProps[p_PidLidClipStart].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidClipStart],PT_SYSTIME);
         spvProps[p_PidLidClipEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidClipEnd],PT_SYSTIME);
         spvProps[p_PidLidTimeZoneStruct].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTimeZoneStruct],PT_BINARY);
         spvProps[p_PidLidTimeZoneDescription].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTimeZoneDescription],PT_UNICODE);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].ulPropTag
           = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionRecur],
           PT_BINARY);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionStartDisplay],
            PT_BINARY);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentTimeZoneDefinitionEndDisplay],
            PT_BINARY);
         spvProps[p_PidLidAppointmentRecur].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidAppointmentRecur],PT_BINARY);
         spvProps[p_PidLidRecurrenceType].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurrenceType],PT_LONG);
         spvProps[p_PidLidRecurrencePattern].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidRecurrencePattern],PT_UNICODE);
         spvProps[p_PidLidIsRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidIsRecurring],PT_BOOLEAN);
         spvProps[p_PidLidGlobalObjectId].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidGlobalObjectId],PT_BINARY);
         spvProps[p_PidLidCleanGlobalObjectId].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCleanGlobalObjectId],PT_BINARY);
         spvProps[p_PidLidCommonStart].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonStart],PT_SYSTIME);
         spvProps[p_PidLidCommonEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonEnd],PT_SYSTIME);
         spvProps[p_PidLidSideEffects].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidSideEffects],PT_LONG);
         spvProps[p_PR_SUBJECT_W].ulPropTag          = PR_SUBJECT_W;
         spvProps[p_PR_START_DATE].ulPropTag         = PR_START_DATE;
         spvProps[p_PR_END_DATE].ulPropTag           = PR_END_DATE;
         spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag    = PR_MESSAGE_CLASS_W;
         spvProps[p_PR_ICON_INDEX].ulPropTag         = PR_ICON_INDEX;
         spvProps[p_PR_CONVERSATION_INDEX].ulPropTag   = PR_CONVERSATION_INDEX;
         spvProps[p_PR_MESSAGE_FLAGS].ulPropTag      = PR_MESSAGE_FLAGS;
         spvProps[p_PidLidAppointmentSequence].Value.l = 0;
         spvProps[p_PidLidBusyStatus].Value.l = olBusy;
         spvProps[p_PidLidLocation].Value.lpszW = szLocation;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PidLidAppointmentStartWhole].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PidLidAppointmentEndWhole].Value.ft);
         spvProps[p_PidLidAppointmentDuration].Value.l = ulDuration;
         spvProps[p_PidLidAppointmentColor].Value.l = 0; // No color
         spvProps[p_PidLidResponseStatus].Value.l = respNone;
         spvProps[p_PidLidRecurring].Value.b = true;
         SystemTimeToFileTime(lpszClipStartUST,&spvProps[p_PidLidClipStart].Value.ft);
         SystemTimeToFileTime(lpstClipEndUST,&spvProps[p_PidLidClipEnd].Value.ft);
         SYSTEMTIME stStandard = {0};
         stStandard.wMonth = 0xB;
         stStandard.wDay = 0x1;
         stStandard.wHour = 0x2;
         SYSTEMTIME stDaylight = {0};
         stDaylight.wMonth = 0x3;
         stDaylight.wDay = 0x2;
         stDaylight.wHour = 0x2;
         hRes = BuildTimeZoneStruct(
            300,
            0,
            (DWORD)-60,
            &stStandard,
            &stDaylight,
            &spvProps[p_PidLidTimeZoneStruct].Value.bin.cb,
            &spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb);
         spvProps[p_PidLidTimeZoneDescription].Value.lpszW = L"(GMT-05:00) Eastern Time (US & Canada)";
         SYSTEMTIME stRule1Standard = {0};
         stRule1Standard.wMonth = 0xA;
         stRule1Standard.wDay = 0x5;
         stRule1Standard.wHour = 0x2;
         SYSTEMTIME stRule1Daylight = {0};
         stRule1Daylight.wMonth = 0x4;
         stRule1Daylight.wDay = 0x1;
         stRule1Daylight.wHour = 0x2;
         if (SUCCEEDED(hRes)) hRes = BuildTimeZoneDefinition(
            L"Eastern Standard Time",
            0, // TZRule Flags
            2006, // wYear
            300, // lbias
            0, // lStandardBias,
            (DWORD)-60, // lDaylightBias,
            &stRule1Standard, // stStandardDate
            &stRule1Daylight, // stDaylightDate
            TZRULE_FLAG_EFFECTIVE_TZREG, // TZRule Flags
            2007, // wYear
            300, // lbias
            0, // lStandardBias,
            (DWORD)-60, // lDaylightBias,
            &stStandard, // stStandardDate
            &stDaylight, // stDaylightDate
            &spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb,
            &spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb);
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].Value.bin.cb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionStartDisplay].Value.bin.lpb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].Value.bin.cb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.cb;
         spvProps[p_PidLidAppointmentTimeZoneDefinitionEndDisplay].Value.bin.lpb
            = spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         if (SUCCEEDED(hRes)) hRes = BuildWeeklyAppointmentRecurrencePattern(
            lpstStartDateLocal,
            lpstEndDateLocal,
            lpstFirstDOW,
            dwStartOffsetLocal,
            dwEndOffsetLocal,
            dwPeriod,
            dwOccurrenceCount,
            dwPatternTypeSpecific,
            &spvProps[p_PidLidAppointmentRecur].Value.bin.cb,
            &spvProps[p_PidLidAppointmentRecur].Value.bin.lpb);
         spvProps[p_PidLidRecurrenceType].Value.l = rectypeWeekly;
         spvProps[p_PidLidRecurrencePattern].Value.lpszW = szPattern;
         spvProps[p_PidLidIsRecurring].Value.b = true;
         if (SUCCEEDED(hRes)) hRes = BuildGlobalObjectId(
            &spvProps[p_PidLidGlobalObjectId].Value.bin.cb,
            &spvProps[p_PidLidGlobalObjectId].Value.bin.lpb);
         spvProps[p_PidLidCleanGlobalObjectId].Value.bin.cb  = spvProps[p_PidLidGlobalObjectId].Value.bin.cb;
         spvProps[p_PidLidCleanGlobalObjectId].Value.bin.lpb = spvProps[p_PidLidGlobalObjectId].Value.bin.lpb;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PidLidCommonStart].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PidLidCommonEnd].Value.ft);
         spvProps[p_PidLidSideEffects].Value.l
            = seOpenToDelete | seOpenToCopy | seOpenToMove | seCoerceToInbox | seOpenForCtxMenu;
         spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
         SystemTimeToFileTime(lpstStartFirstUST,&spvProps[p_PR_START_DATE].Value.ft);
         SystemTimeToFileTime(lpstEndFirstUST,&spvProps[p_PR_END_DATE].Value.ft);
         spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Appointment";
         spvProps[p_PR_ICON_INDEX].Value.l = 0x00000401; // Recurring Appointment
         if (SUCCEEDED(hRes)) hRes = BuildConversationIndex(
            &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
            &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
         spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_READ;
         if (SUCCEEDED(hRes)) hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = lpMessage->SaveChanges(FORCE_SAVE);
         }
         if (spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb)
            delete[] spvProps[p_PidLidTimeZoneStruct].Value.bin.lpb;
         if (spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb)
            delete[] spvProps[p_PidLidAppointmentTimeZoneDefinitionRecur].Value.bin.lpb;
         // Do not delete p_PidLidAppointmentTimeZoneDefinitionStartDisplay, 
         // it was borrowed from p_PidLidAppointmentTimeZoneDefinitionStartDisplay
         // Do not delete p_PidLidAppointmentTimeZoneDefinitionEndDisplay, 
         // it was borrowed from p_PidLidAppointmentTimeZoneDefinitionStartDisplay
         if (spvProps[p_PidLidAppointmentRecur].Value.bin.lpb)
            delete[] spvProps[p_PidLidAppointmentRecur].Value.bin.lpb;
         if (spvProps[p_PidLidGlobalObjectId].Value.bin.lpb)
            delete[] spvProps[p_PidLidGlobalObjectId].Value.bin.lpb;
         // Do not delete p_PidLidCleanGlobalObjectId, it was borrowed from p_PidLidGlobalObjectId
         if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
            delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
      }
      MAPIFreeBuffer(lpNamedPropTags);
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}

```

## <a name="see-also"></a><span data-ttu-id="76f63-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76f63-141">See also</span></span>

- [<span data-ttu-id="76f63-142">Verwenden von MAPI zum Erstellen Outlook 2007-Elementen</span><span class="sxs-lookup"><span data-stu-id="76f63-142">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

