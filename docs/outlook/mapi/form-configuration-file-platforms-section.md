---
title: Abschnitt "Formularkonfigurationsdatei [Plattformen]
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7439de5b91cefe89eba2f9395595d4a7c8ca3ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419128"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="216db-103">Abschnitt "Formularkonfigurationsdatei [Plattformen]</span><span class="sxs-lookup"><span data-stu-id="216db-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="216db-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="216db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="216db-105">Im **Abschnitt [Plattformen]** wird der vollständige Satz von Plattformen aufgeführt, die von diesem Formular unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="216db-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="216db-106">Jeder Plattformeintrag besteht aus dem Präfix **Plattform.**</span><span class="sxs-lookup"><span data-stu-id="216db-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="216db-107">_string_, wobei  _string_ ein beliebiger Zeichenfolgencode für die Plattform ist.</span><span class="sxs-lookup"><span data-stu-id="216db-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="216db-108">Jede Zeichenfolge entspricht dem **CPU-Eintrag** eines einzelnen **[Platforms]-Abschnitts.**</span><span class="sxs-lookup"><span data-stu-id="216db-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="216db-109">Jeder Eintrag in einem **Abschnitt [Plattformen]** definiert eine  _Plattformzeichenfolge,_ die auf eine nachfolgende **[Plattform] verweist.**</span><span class="sxs-lookup"><span data-stu-id="216db-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="216db-110">_Platform string_ **]** section, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="216db-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="216db-111">Im **Abschnitt [Plattformen]** wird der vollständige Satz von Plattformen aufgeführt, die von diesem Formular unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="216db-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="216db-112">Jeder Plattformeintrag besteht aus dem Präfix **Plattform.**</span><span class="sxs-lookup"><span data-stu-id="216db-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="216db-113">_string_, wobei  _string_ ein beliebiger Zeichenfolgencode für die Plattform ist.</span><span class="sxs-lookup"><span data-stu-id="216db-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="216db-114">Jede Zeichenfolge entspricht dem **CPU-Eintrag** eines einzelnen **[Platforms]-Abschnitts.**</span><span class="sxs-lookup"><span data-stu-id="216db-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="216db-115">Jeder Eintrag in einem **Abschnitt [Plattformen]** definiert eine  _Plattformzeichenfolge,_ die auf eine nachfolgende **[Plattform] verweist.**</span><span class="sxs-lookup"><span data-stu-id="216db-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="216db-116">_Platform string_ **]** section, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="216db-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="216db-117">**[Plattformen]**</span><span class="sxs-lookup"><span data-stu-id="216db-117">**[Platforms]**</span></span>
  
<span data-ttu-id="216db-118">**Plattform**.</span><span class="sxs-lookup"><span data-stu-id="216db-118">**Platform**.</span></span> <span data-ttu-id="216db-119">_string_  =   _Plattformzeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="216db-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="216db-120">Im Folgenden finden Sie ein Beispiel für einen **Abschnitt [Plattformen].**</span><span class="sxs-lookup"><span data-stu-id="216db-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="216db-121">Jede **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="216db-121">Each **[Platform.**</span></span> <span data-ttu-id="216db-122">_Platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="216db-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="216db-123">Der **CPU-Eintrag** gibt den Prozessor an, und der **OSVersion-Eintrag** gibt das Betriebssystem an.</span><span class="sxs-lookup"><span data-stu-id="216db-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="216db-124">Gültige **CPU-Werte** werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="216db-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="216db-125">**CPU-Eintrag**</span><span class="sxs-lookup"><span data-stu-id="216db-125">**CPU Entry**</span></span>|<span data-ttu-id="216db-126">**Prozessor**</span><span class="sxs-lookup"><span data-stu-id="216db-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="216db-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="216db-127">Ix86</span></span>  <br/> |<span data-ttu-id="216db-128">Intel 80x86- und Pentium-Prozessoren sowie gleichwertige Prozessoren von AMD, Cyrix, NextGen und anderen Herstellern.</span><span class="sxs-lookup"><span data-stu-id="216db-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="216db-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="216db-129">MIPS</span></span>  <br/> |<span data-ttu-id="216db-130">MIPS R4000-Prozessorreihe.</span><span class="sxs-lookup"><span data-stu-id="216db-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="216db-131">AXP</span><span class="sxs-lookup"><span data-stu-id="216db-131">AXP</span></span>  <br/> |<span data-ttu-id="216db-132">Digital Equipment Corporation Alpha AXP-Prozessor.</span><span class="sxs-lookup"><span data-stu-id="216db-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="216db-133">PPC</span><span class="sxs-lookup"><span data-stu-id="216db-133">PPC</span></span>  <br/> |<span data-ttu-id="216db-134">Prozessoren der Power -PC-Serie von Motorola.</span><span class="sxs-lookup"><span data-stu-id="216db-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="216db-135">M68</span><span class="sxs-lookup"><span data-stu-id="216db-135">M68</span></span>  <br/> |<span data-ttu-id="216db-136">Prozessoren der Serie "68x00" von "68x00".</span><span class="sxs-lookup"><span data-stu-id="216db-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="216db-137">Gültige **OSVersion-Werte** werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="216db-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="216db-138">**OSVersion-Eintrag**</span><span class="sxs-lookup"><span data-stu-id="216db-138">**OSVersion Entry**</span></span>|<span data-ttu-id="216db-139">**Betriebssystem**</span><span class="sxs-lookup"><span data-stu-id="216db-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="216db-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="216db-140">Win3.1</span></span>  <br/> |<span data-ttu-id="216db-141">Windows 3.1 und Windows workgroups 3.11.</span><span class="sxs-lookup"><span data-stu-id="216db-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="216db-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="216db-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="216db-143">Windows NT 3.5 oder niedriger.</span><span class="sxs-lookup"><span data-stu-id="216db-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="216db-144">Win95</span><span class="sxs-lookup"><span data-stu-id="216db-144">Win95</span></span>  <br/> |<span data-ttu-id="216db-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="216db-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="216db-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="216db-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="216db-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="216db-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="216db-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="216db-148">Mac7</span></span>  <br/> |<span data-ttu-id="216db-149">Macintosh System 7.</span><span class="sxs-lookup"><span data-stu-id="216db-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="216db-150">Darüber hinaus die **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="216db-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="216db-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span><span class="sxs-lookup"><span data-stu-id="216db-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="216db-152">Der **Eintrag Datei** listet die ausführbare Datei der Formularserveranwendung auf, die von der Formularbibliothek verwaltet und beim Starten des Formulars in ein neues Unterverzeichnis im Datenträgercache geladen wird.</span><span class="sxs-lookup"><span data-stu-id="216db-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="216db-153">Wenn stattdessen **ein LinkTo-Eintrag** verwendet wird, enthält er den Namen einer anderen Plattformzeichenfolge, aus der die **Dateiinformationen** übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="216db-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="216db-154">Dies ist hilfreich, wenn eine Version eines Formulars mehrere Plattformen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="216db-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="216db-155">Der **Registrierungseintrag** wird immer dann verwendet, wenn der Eintrag **Datei** verwendet wird. Er identifiziert den Registrierungsschlüssel für die Formularbibliothek, in der die ausführbare Datei für die Formularserveranwendung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="216db-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="216db-156">Zeichenfolgen, denen ein umgekehrter Schrägstrich ( \ ) vorangehen, werden am Stamm der Registrierung platziert.</span><span class="sxs-lookup"><span data-stu-id="216db-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="216db-157">Zeichenfolgen, denen kein umgekehrter Schrägstrich vorangegangen ist, werden im HKEY_CLASSES_ROOT\CLSID\  _GUID_\ Registrierungsschlüssel platziert, wobei  _GUID_ die **GUID** des Formulars ist.</span><span class="sxs-lookup"><span data-stu-id="216db-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="216db-158">Die Zeichen "%d" können verwendet werden, um den Pfadnamen des Verzeichnisses anzugeben, aus dem die Formularkonfigurationsdatei gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="216db-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="216db-159">Dies ist hilfreich, um andere Dateien mit Pfadnamen relativ zur Formularkonfigurationsdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="216db-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="216db-160">**Mehrere Datei-** **oder Registrierungseinträge** können mithilfe von Datei oder Registrierung als Präfix gefolgt von einem beliebigen anderen Text angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="216db-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="216db-161">Das Format für **die [Plattform.**</span><span class="sxs-lookup"><span data-stu-id="216db-161">The format for the **[Platform.**</span></span> <span data-ttu-id="216db-162">_platform string_ **]** section is:</span><span class="sxs-lookup"><span data-stu-id="216db-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="216db-163">**[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="216db-163">**[Platform.**</span></span> <span data-ttu-id="216db-164">_Plattformzeichenfolge_ **]**</span><span class="sxs-lookup"><span data-stu-id="216db-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="216db-165">**CPU**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="216db-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="216db-166">**OSVersion**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="216db-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="216db-167">**Datei**  =   _path_</span><span class="sxs-lookup"><span data-stu-id="216db-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="216db-168">**LinkTo**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="216db-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="216db-169">**Registrierung**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="216db-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="216db-170">Im Folgenden finden Sie zwei Beispiele **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="216db-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="216db-171">_Platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span><span class="sxs-lookup"><span data-stu-id="216db-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
```cpp
[Platform.NTx86]
CPU = ix86
OSVersion = WinNT3.5
File = \helpdesk.exe
Registry = Local Server = %d\helpdesk.exe
[Platform.Win95]
CPU = ix86
OSVersion = Win95
LinkTo = NTx86

```

<span data-ttu-id="216db-172">Die **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="216db-172">The **[Platform.**</span></span> <span data-ttu-id="216db-173">_Der_ Abschnitt plattformzeichenfolge **]** wird beim Hinzufügen eines Formulars zur lokalen Formularbibliothek ignoriert, wenn davon ausgegangen wird, dass das Installationsprogramm die Dateien, die den Nachrichtenklassenhandler bilden, in den verfügbaren lokalen Speicher wie im Abschnitt des Handlers in der OLE-Registrierung benannt platziert hat und die OLE-Registrierung in der Registrierung des Systems durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="216db-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

