---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialisiert ein IOlkApptRebaser-Objekt für die Verwendung in Neuzuordnen Termine im Outlook-Kalender.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397541"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="26192-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="26192-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="26192-104">Initialisiert ein [IOlkApptRebaser](iolkapptrebaser.md) -Objekt für die Verwendung in Neuzuordnen Termine im Outlook-Kalender.</span><span class="sxs-lookup"><span data-stu-id="26192-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="26192-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="26192-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26192-106">Headerdatei:</span><span class="sxs-lookup"><span data-stu-id="26192-106">Header file:</span></span>  <br/> |<span data-ttu-id="26192-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="26192-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="26192-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="26192-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="26192-109">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="26192-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="26192-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="26192-110">Called by:</span></span>  <br/> |<span data-ttu-id="26192-111">MAPI-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="26192-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="26192-112">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="26192-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="26192-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="26192-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="26192-114">DLL-Einstiegspunkt:</span><span class="sxs-lookup"><span data-stu-id="26192-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="26192-115">**HrCreateApptRebaser@44**</span><span class="sxs-lookup"><span data-stu-id="26192-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a><span data-ttu-id="26192-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="26192-116">Parameters</span></span>

<span data-ttu-id="26192-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26192-117">_ulFlags_</span></span>
  
> <span data-ttu-id="26192-118">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26192-118">[in] Required.</span></span> <span data-ttu-id="26192-119">Eine Bitmaske der Flags verwendet, um zu steuern, wie Neuzuordnen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26192-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="26192-120">Die folgenden Kennzeichen können festgelegt werden und sind in tzmovelib.h definiert:</span><span class="sxs-lookup"><span data-stu-id="26192-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="26192-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** – Terminelemente, in dem der Benutzer der Organisator der Besprechung ist, zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="26192-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="26192-122">Beachten Sie, dass in der Standardeinstellung dadurch Outlook senden besprechungsaktualisierungen an alle Teilnehmer einer Sitzung zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="26192-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="26192-123">Sie können dieses Flag kombinieren, mit **REBASE_FLAG_FORCE_NO_EX_UPDATES** oder **REBASE_FLAG_FORCE_NO_UPDATES** ändern, wie die Besprechung aktualisiert behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="26192-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="26192-124">**REBASE_FLAG_UPDATE_UNMARKED** – aktualisieren Terminelemente, die nicht gekennzeichnet wurden mit einer Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="26192-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="26192-125">Wenn dieses Flag angegeben wird, wird der *pTZMissing* Wert als die Zeitzone, die in ein Element erstellt wird für alle Elemente verwendet, die nicht Zeitzonendaten verfügen.</span><span class="sxs-lookup"><span data-stu-id="26192-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="26192-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** – nur Termin Terminserien aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="26192-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="26192-127">**REBASE_FLAG_NO_UI** – einschließlich Anmeldung Dialogfelder angezeigt, in der Regel beim Öffnen eines Nachrichtenspeichers Benutzeroberfläche (UI), nicht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="26192-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="26192-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** – führen Sie nicht einer Terminelemente, die in der Vergangenheit auftreten.</span><span class="sxs-lookup"><span data-stu-id="26192-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="26192-129">**REBASE_FLAG_FORCE_REBASE** – nicht den Organisator zum Neuzuordnen von Entscheidungen prüfen, aber einer Terminelemente, in dem der Benutzer ein Teilnehmer ist.</span><span class="sxs-lookup"><span data-stu-id="26192-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="26192-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** – senden nur aktualisiert, wenn der Benutzer der Organisator ist und Empfänger nicht mit einem Exchange-Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="26192-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="26192-131">**REBASE_FLAG_FORCE_NO_UPDATES** – Updates nie senden.</span><span class="sxs-lookup"><span data-stu-id="26192-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="26192-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** – einer nur Einzel-Instanz Terminelemente erstellt, bevor der Patch angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="26192-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="26192-133">**REBASE_FLAG_REPORTING_MODE** – nicht tatsächlich Rebase ausführen, würde nur Bericht Termin Elemente, die zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="26192-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="26192-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** – besprechungsaktualisierungen auf Ressourcen zu senden.</span><span class="sxs-lookup"><span data-stu-id="26192-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="26192-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="26192-135">_pSession_</span></span>
  
> <span data-ttu-id="26192-136">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26192-136">[in] Required.</span></span> <span data-ttu-id="26192-137">Ein Zeiger auf eine MAPI-Sitzung-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="26192-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="26192-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="26192-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="26192-139">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26192-139">[in] Required.</span></span> <span data-ttu-id="26192-140">Ein Zeiger auf einen Nachrichtenspeicher mit Terminelemente zu zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="26192-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="26192-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="26192-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="26192-142">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26192-142">[in] Required.</span></span> <span data-ttu-id="26192-143">Ein Zeiger auf einen Kalenderordner mit Terminelemente zu zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="26192-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="26192-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="26192-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="26192-145">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="26192-145">[in] Optional.</span></span> <span data-ttu-id="26192-146">Ein Zeiger auf eine Zeichenfolge mit dem Präfix, das auf Besprechungsanfragen vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="26192-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="26192-147">NULL kann sein.</span><span class="sxs-lookup"><span data-stu-id="26192-147">May be NULL.</span></span>
    
<span data-ttu-id="26192-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="26192-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="26192-149">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="26192-149">[in] Optional.</span></span> <span data-ttu-id="26192-150">Der Zeitzone Patch installieren Datum.</span><span class="sxs-lookup"><span data-stu-id="26192-150">The time zone patch install date.</span></span> <span data-ttu-id="26192-151">Nur verwendet, wenn das Flag **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="26192-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="26192-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="26192-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="26192-153">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="26192-153">[in] Optional.</span></span> <span data-ttu-id="26192-154">Die Erweiterung Tiefe beim Empfänger ausschließen listet Verteilerlisten mit Exchange Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="26192-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="26192-155">Nur verwendet, wenn das Flag **REBASE_FLAG_FORCE_NO_EX_UPDATES** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="26192-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="26192-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="26192-156">_pTZTo_</span></span>
  
> <span data-ttu-id="26192-157">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26192-157">[in] Required.</span></span> <span data-ttu-id="26192-158">Ein Zeiger auf eine **TZDEFINITION** -Struktur, beschreibt die Zeitzone, um zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="26192-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="26192-159">**TZDEFINITION** ist in Tzmovelib definiert.</span><span class="sxs-lookup"><span data-stu-id="26192-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="26192-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="26192-160">pTZMissing</span></span>
  
> <span data-ttu-id="26192-161">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="26192-161">[in] Required.</span></span> <span data-ttu-id="26192-162">Ein Zeiger auf eine **TZDEFINITION** -Struktur, beschreibt die Zeitzone um betrachtet werden, wenn die Informationen zur Zeitzone für ein Element nicht versehen ist.</span><span class="sxs-lookup"><span data-stu-id="26192-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="26192-163">Darf nicht NULL, aber nur sein verwendet, wenn das Flag **REBASE_FLAG_UPDATE_UNMARKED** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="26192-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="26192-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="26192-164">_ppError_</span></span>
  
> <span data-ttu-id="26192-165">[out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR** -Struktur, die Angaben zu Version, Komponente und Kontext für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="26192-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="26192-166">NULL, wenn keine erweiterten Fehlerinformationen erwünscht ist.</span><span class="sxs-lookup"><span data-stu-id="26192-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="26192-167">Mit [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx)frei.</span><span class="sxs-lookup"><span data-stu-id="26192-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="26192-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="26192-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="26192-169">[out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle **IOlkApptRebaser** .</span><span class="sxs-lookup"><span data-stu-id="26192-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="26192-170">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="26192-170">Return values</span></span>

<span data-ttu-id="26192-171">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="26192-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26192-172">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="26192-172">Remarks</span></span>

<span data-ttu-id="26192-173">Wenn [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) für die Adresse des dieser Funktion in tzmovelib.dll suchen, geben Sie **HrCreateApptRebaser@44** als den Namen der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="26192-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="26192-174">Nicht alle der Werte sind gültig in Kombination mit anderen.</span><span class="sxs-lookup"><span data-stu-id="26192-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="26192-175">Weitere Informationen zu den verschiedenen Optionen finden Sie im Abschnitt "Glossar mit Befehlszeilenoptionen für die Outlook-Zeitzone Aktualisierungstool" in [KB 931667: wie Adresse, Zeitzone Änderungen mithilfe der Zeit Zeitzonendaten für Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span><span class="sxs-lookup"><span data-stu-id="26192-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26192-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26192-176">See also</span></span>

- [<span data-ttu-id="26192-177">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="26192-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

