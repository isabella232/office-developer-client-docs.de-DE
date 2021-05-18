---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialisiert ein IOlkApptRebaser-Objekt zur Verwendung beim Neubasieren von Terminen in Outlook Kalendern.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317612"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="13fa2-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="13fa2-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="13fa2-104">Initialisiert ein [IOlkApptRebaser-Objekt](iolkapptrebaser.md) zur Verwendung beim Neubasieren von Terminen in Outlook Kalendern.</span><span class="sxs-lookup"><span data-stu-id="13fa2-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="13fa2-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="13fa2-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13fa2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="13fa2-106">Header file:</span></span>  <br/> |<span data-ttu-id="13fa2-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="13fa2-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="13fa2-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="13fa2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="13fa2-109">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="13fa2-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="13fa2-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="13fa2-110">Called by:</span></span>  <br/> |<span data-ttu-id="13fa2-111">MAPI-Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="13fa2-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="13fa2-112">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="13fa2-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="13fa2-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="13fa2-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="13fa2-114">DLL-Einstiegspunkt:</span><span class="sxs-lookup"><span data-stu-id="13fa2-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="13fa2-115">**HrCreateApptRebaser@44**</span><span class="sxs-lookup"><span data-stu-id="13fa2-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="13fa2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="13fa2-116">Parameters</span></span>

<span data-ttu-id="13fa2-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="13fa2-117">_ulFlags_</span></span>
  
> <span data-ttu-id="13fa2-118">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13fa2-118">[in] Required.</span></span> <span data-ttu-id="13fa2-119">Eine Bitmaske mit Flags, die zum Steuern der Neubasierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13fa2-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="13fa2-120">Die folgenden Flags können festgelegt werden und sind in tzmovelib.h definiert:</span><span class="sxs-lookup"><span data-stu-id="13fa2-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="13fa2-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** – Terminelemente, bei denen der Benutzer der Besprechungsorganisator ist, werden neu basisiert.</span><span class="sxs-lookup"><span data-stu-id="13fa2-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="13fa2-122">Beachten Sie, dass dies standardmäßig dazu führt, Outlook Besprechungsupdates an alle Teilnehmer einer besprechungsbasierten Besprechung senden.</span><span class="sxs-lookup"><span data-stu-id="13fa2-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="13fa2-123">Sie können dieses Flag mit REBASE_FLAG_FORCE_NO_EX_UPDATES **oder** REBASE_FLAG_FORCE_NO_UPDATES, um die Art und **Weise** zu ändern, wie Besprechungsupdates behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="13fa2-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="13fa2-124">**REBASE_FLAG_UPDATE_UNMARKED** –Terminelemente aktualisieren, die nicht mit einer Zeitzone markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="13fa2-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="13fa2-125">Wenn dieses Flag angegeben wird, wird der  *pTZMissing-Wert*  als Zeitzone verwendet, in der ein Element für alle Elemente erstellt wird, die keine Zeitzonendaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="13fa2-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="13fa2-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** – Nur Terminserienelemente aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="13fa2-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="13fa2-127">**REBASE_FLAG_NO_UI** – Keine Benutzeroberfläche anzeigen, einschließlich Anmeldedialogfeldern, die beim Öffnen eines Nachrichtenspeichers in der Regel angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="13fa2-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="13fa2-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** – In der Vergangenheit vorkommende Terminelemente dürfen nicht neu basierten werden.</span><span class="sxs-lookup"><span data-stu-id="13fa2-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="13fa2-129">**REBASE_FLAG_FORCE_REBASE** – Überprüfen Sie den Organisator nicht auf die Neubasierung von Entscheidungen, sondern erstellen Sie terminbezogene Elemente, bei denen der Benutzer ein Teilnehmer ist, neu.</span><span class="sxs-lookup"><span data-stu-id="13fa2-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="13fa2-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** – Aktualisierungen nur senden, wenn der Benutzer der Organisator ist und der Empfänger nicht mit einer Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13fa2-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="13fa2-131">**REBASE_FLAG_FORCE_NO_UPDATES** – Niemals Updates senden.</span><span class="sxs-lookup"><span data-stu-id="13fa2-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="13fa2-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** – Basierten Sie nur Terminelemente mit einer Instanz neu, die vor dem Anwenden des Patches erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="13fa2-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="13fa2-133">**REBASE_FLAG_REPORTING_MODE** – Erstellen Sie keine rebase, sondern melden Sie lediglich Terminelemente, die neubasiert würden.</span><span class="sxs-lookup"><span data-stu-id="13fa2-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="13fa2-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** – Senden von Besprechungsupdates an Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="13fa2-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="13fa2-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="13fa2-135">_pSession_</span></span>
  
> <span data-ttu-id="13fa2-136">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13fa2-136">[in] Required.</span></span> <span data-ttu-id="13fa2-137">Ein Zeiger auf eine MAPI-Sitzungsschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="13fa2-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="13fa2-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="13fa2-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="13fa2-139">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13fa2-139">[in] Required.</span></span> <span data-ttu-id="13fa2-140">Ein Zeiger auf einen Nachrichtenspeicher, der neu zu erstellende Terminelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="13fa2-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="13fa2-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="13fa2-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="13fa2-142">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13fa2-142">[in] Required.</span></span> <span data-ttu-id="13fa2-143">Ein Zeiger auf einen Kalenderordner, der neu zu erstellende Terminelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="13fa2-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="13fa2-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="13fa2-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="13fa2-145">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="13fa2-145">[in] Optional.</span></span> <span data-ttu-id="13fa2-146">Ein Zeiger auf eine Zeichenfolge, die das Präfix enthält, das für Besprechungsanfragen vorangestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="13fa2-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="13fa2-147">Kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="13fa2-147">May be NULL.</span></span>
    
<span data-ttu-id="13fa2-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="13fa2-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="13fa2-149">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="13fa2-149">[in] Optional.</span></span> <span data-ttu-id="13fa2-150">Das Installationsdatum des Zeitzonenpatches.</span><span class="sxs-lookup"><span data-stu-id="13fa2-150">The time zone patch install date.</span></span> <span data-ttu-id="13fa2-151">Wird nur verwendet, **wenn REBASE_FLAG_ONLY_CREATED_PRE_PATCH** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="13fa2-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="13fa2-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="13fa2-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="13fa2-153">[in] Optional.</span><span class="sxs-lookup"><span data-stu-id="13fa2-153">[in] Optional.</span></span> <span data-ttu-id="13fa2-154">Die Erweiterungstiefe beim Erweitern von Verteilerlisten, um Empfänger auszuschließen, die mit Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13fa2-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="13fa2-155">Wird nur verwendet, **wenn REBASE_FLAG_FORCE_NO_EX_UPDATES** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="13fa2-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="13fa2-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="13fa2-156">_pTZTo_</span></span>
  
> <span data-ttu-id="13fa2-157">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13fa2-157">[in] Required.</span></span> <span data-ttu-id="13fa2-158">Ein Zeiger auf eine **TZDEFINITION-Struktur,** in der die Zeitzone beschrieben wird, in der eine erneute Datenbank verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="13fa2-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="13fa2-159">**TZDEFINITION** ist in tzmovelib definiert.</span><span class="sxs-lookup"><span data-stu-id="13fa2-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="13fa2-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="13fa2-160">pTZMissing</span></span>
  
> <span data-ttu-id="13fa2-161">[in] Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13fa2-161">[in] Required.</span></span> <span data-ttu-id="13fa2-162">Ein Zeiger auf eine **TZDEFINITION-Struktur,** die die anzunehmende Zeitzone beschreibt, wenn Zeitzoneninformationen nicht für ein Element gestempelt werden.</span><span class="sxs-lookup"><span data-stu-id="13fa2-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="13fa2-163">Darf nicht NULL sein, sondern nur verwendet werden, wenn **das REBASE_FLAG_UPDATE_UNMARKED** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="13fa2-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="13fa2-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="13fa2-164">_ppError_</span></span>
  
> <span data-ttu-id="13fa2-165">[out] Ein Zeiger auf einen Zeiger auf eine **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="13fa2-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="13fa2-166">Kann NULL sein, wenn keine erweiterten Fehlerinformationen gewünscht werden.</span><span class="sxs-lookup"><span data-stu-id="13fa2-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="13fa2-167">Kostenlos mit [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="13fa2-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="13fa2-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="13fa2-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="13fa2-169">[out] Ein Zeiger auf einen Zeiger auf die **zurückgegebene IOlkApptRebaser-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="13fa2-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="13fa2-170">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="13fa2-170">Return values</span></span>

<span data-ttu-id="13fa2-171">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="13fa2-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13fa2-172">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13fa2-172">Remarks</span></span>

<span data-ttu-id="13fa2-173">Wenn Sie [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) zum Suchen nach der Adresse dieser Funktion in tzmovelib.dll verwenden, geben Sie HrCreateApptRebaser@44 **Prozedurnamen** an.</span><span class="sxs-lookup"><span data-stu-id="13fa2-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="13fa2-174">Nicht alle Flags sind in Kombination miteinander gültig.</span><span class="sxs-lookup"><span data-stu-id="13fa2-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="13fa2-175">Weitere Informationen zu den verschiedenen Optionen finden Sie im Abschnitt "Glossar der Befehlszeilenoptionen für das Outlook Time Zone Data Update Tool" in [KB 931667:](https://support.microsoft.com/kb/931667/en-us)How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook .</span><span class="sxs-lookup"><span data-stu-id="13fa2-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="13fa2-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13fa2-176">See also</span></span>

- [<span data-ttu-id="13fa2-177">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="13fa2-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

