---
title: Abschnitt [Platforms] in der Formularkonfigurationsdatei
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3b9b3dc0-4f82-468b-8e77-0374c5b196f4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ddc6db2303d9d5f114fdb27b6e15e699a04e73f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791722"
---
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="e200d-103">Abschnitt [Platforms] in der Formularkonfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="e200d-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="e200d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e200d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e200d-105">Im Abschnitt **[Plattformen]** der vollständigen Satz von Plattformen, die von diesem Formular aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e200d-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="e200d-106">Jeder Eintrag Plattform besteht aus dem Präfix **Plattform.**</span><span class="sxs-lookup"><span data-stu-id="e200d-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="e200d-107">_Zeichenfolge_in der _Zeichenfolge_ eine beliebige Zeichenfolge Code für die Plattform ist.</span><span class="sxs-lookup"><span data-stu-id="e200d-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="e200d-108">Jede Zeichenfolge entspricht dem Eintrag **CPU** , der eine einzelne Abschnitte **[Plattformen]** .</span><span class="sxs-lookup"><span data-stu-id="e200d-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="e200d-109">Jeder Eintrag in einem Abschnitt **[Plattformen]** definiert eine _Plattformzeichenfolge_ , die eine nachfolgende verweist auf **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="e200d-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="e200d-110">_Plattformzeichenfolge_ **]** Abschnitt wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e200d-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="e200d-111">Im Abschnitt **[Plattformen]** der vollständigen Satz von Plattformen, die von diesem Formular aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e200d-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="e200d-112">Jeder Eintrag Plattform besteht aus dem Präfix **Plattform.**</span><span class="sxs-lookup"><span data-stu-id="e200d-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="e200d-113">_Zeichenfolge_in der _Zeichenfolge_ eine beliebige Zeichenfolge Code für die Plattform ist.</span><span class="sxs-lookup"><span data-stu-id="e200d-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="e200d-114">Jede Zeichenfolge entspricht dem Eintrag **CPU** , der eine einzelne Abschnitte **[Plattformen]** .</span><span class="sxs-lookup"><span data-stu-id="e200d-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="e200d-115">Jeder Eintrag in einem Abschnitt **[Plattformen]** definiert eine _Plattformzeichenfolge_ , die eine nachfolgende verweist auf **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="e200d-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="e200d-116">_Plattformzeichenfolge_ **]** Abschnitt wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e200d-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="e200d-117">**[Plattformen]**</span><span class="sxs-lookup"><span data-stu-id="e200d-117">**[Platforms]**</span></span>
  
<span data-ttu-id="e200d-118">**Plattform**.</span><span class="sxs-lookup"><span data-stu-id="e200d-118">**Platform**.</span></span> <span data-ttu-id="e200d-119">_Zeichenfolge_ =  _Plattformzeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="e200d-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="e200d-120">Es folgt ein Beispiel für einen Abschnitt **[Plattformen]** .</span><span class="sxs-lookup"><span data-stu-id="e200d-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="e200d-121">Jede **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="e200d-121">Each **[Platform.**</span></span> <span data-ttu-id="e200d-122">_Plattformzeichenfolge_ **]** Abschnitt enthält zwei erforderliche Einträge **CPU-** und **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="e200d-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="e200d-123">Der **CPU** -Eintrag gibt den Prozessor und der Eintrag **OSVersion** gibt das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="e200d-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="e200d-124">Gültige **CPU** -Werte werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e200d-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="e200d-125">**CPU-Eintrag**</span><span class="sxs-lookup"><span data-stu-id="e200d-125">**CPU Entry**</span></span>|<span data-ttu-id="e200d-126">**Prozessor**</span><span class="sxs-lookup"><span data-stu-id="e200d-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e200d-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="e200d-127">Ix86</span></span>  <br/> |<span data-ttu-id="e200d-128">Intel 80 x 86- und Pentium Prozessoren sowie entsprechende Prozessoren von AMD, Cyrix, NextGen und anderer Hersteller.</span><span class="sxs-lookup"><span data-stu-id="e200d-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="e200d-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="e200d-129">MIPS</span></span>  <br/> |<span data-ttu-id="e200d-130">MIPS R4000 Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="e200d-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="e200d-131">AXP</span><span class="sxs-lookup"><span data-stu-id="e200d-131">AXP</span></span>  <br/> |<span data-ttu-id="e200d-132">Digital Equipment Corporation Alpha AXP Prozessor.</span><span class="sxs-lookup"><span data-stu-id="e200d-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="e200d-133">PPC</span><span class="sxs-lookup"><span data-stu-id="e200d-133">PPC</span></span>  <br/> |<span data-ttu-id="e200d-134">Motorola Power PC Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="e200d-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="e200d-135">M68</span><span class="sxs-lookup"><span data-stu-id="e200d-135">M68</span></span>  <br/> |<span data-ttu-id="e200d-136">Mororola 68 x 00 Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="e200d-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="e200d-137">Gültige Werte für **OSVersion** werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e200d-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="e200d-138">**OSVersion-Eintrag**</span><span class="sxs-lookup"><span data-stu-id="e200d-138">**OSVersion Entry**</span></span>|<span data-ttu-id="e200d-139">**Betriebssystem**</span><span class="sxs-lookup"><span data-stu-id="e200d-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e200d-140">Win3.1</span><span class="sxs-lookup"><span data-stu-id="e200d-140">Win3.1</span></span>  <br/> |<span data-ttu-id="e200d-141">Windows 3.1 und Windows für Arbeitsgruppen 3.11.</span><span class="sxs-lookup"><span data-stu-id="e200d-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="e200d-142">WinNT3.5</span><span class="sxs-lookup"><span data-stu-id="e200d-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="e200d-143">Windows NT 3.5 oder unten.</span><span class="sxs-lookup"><span data-stu-id="e200d-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="e200d-144">Windows 95</span><span class="sxs-lookup"><span data-stu-id="e200d-144">Win95</span></span>  <br/> |<span data-ttu-id="e200d-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="e200d-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="e200d-146">WinNT4.0</span><span class="sxs-lookup"><span data-stu-id="e200d-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="e200d-147">Windows NT 4.0.</span><span class="sxs-lookup"><span data-stu-id="e200d-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="e200d-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="e200d-148">Mac7</span></span>  <br/> |<span data-ttu-id="e200d-149">Macintosh System 7.</span><span class="sxs-lookup"><span data-stu-id="e200d-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="e200d-150">Darüber hinaus die **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="e200d-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="e200d-151">_Plattformzeichenfolge_ **]** Abschnitt muss entweder eine **Datei** oder ein **VerknüpfungMit** Eintrag enthalten.</span><span class="sxs-lookup"><span data-stu-id="e200d-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="e200d-152">**Der Eintrag in der** listet Formular Server ausführbare Datei der Anwendung, die die Formularbibliothek verwaltet und in ein neues Unterverzeichnis im Datenträgercache geladen, wenn das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e200d-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="e200d-153">Wenn Sie ein Eintrag **VerknüpfungMit** stattdessen verwendet wird, enthält den Namen einer anderen Plattform-Zeichenfolge, aus der **die Dateiinformationen** entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="e200d-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="e200d-154">Dies ist nützlich, wenn eine Version eines Formulars mehrere Plattformen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e200d-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="e200d-155">**Der Registrierungseintrag** wird verwendet, wenn **der Eintrag in der** verwendet wird, identifiziert den Registrierungsschlüssel für die Formularbibliothek, in dem die ausführbare Datei für die Server-Anwendung Formular gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="e200d-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="e200d-156">Zeichenfolgen, die durch einen umgekehrten Schrägstrich (\) vorangestellt werden am Stamm der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e200d-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="e200d-157">Zeichenfolgen, die nicht mit einem umgekehrten Schrägstrich vorangestellten befinden sich in der HKEY_CLASSES_ROOT\CLSID\ _GUID_\ Registrierungsschlüssel, wobei _GUID_ die **GUID** des Formulars ist.</span><span class="sxs-lookup"><span data-stu-id="e200d-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="e200d-158">Die Zeichen "%d" können verwendet werden, an der Pfadname des Verzeichnisses, aus dem Lesen der Konfigurationsdatei Formular.</span><span class="sxs-lookup"><span data-stu-id="e200d-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="e200d-159">Dies ist hilfreich für andere Dateien mit Pfadnamen relativ zum Formular Konfigurationsdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="e200d-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="e200d-160">**Mehrere Datei** oder einen **Registrierungsschlüssel** Einträge können mithilfe der Datei oder einen Registrierungsschlüssel als Präfix gefolgt von beliebigen anderen Text angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e200d-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="e200d-161">Das Format für die **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="e200d-161">The format for the **[Platform.**</span></span> <span data-ttu-id="e200d-162">_Plattformzeichenfolge_ **]** Abschnitt ist:</span><span class="sxs-lookup"><span data-stu-id="e200d-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="e200d-163">**[-Plattform.**</span><span class="sxs-lookup"><span data-stu-id="e200d-163">**[Platform.**</span></span> <span data-ttu-id="e200d-164">_Plattformzeichenfolge_ **]**</span><span class="sxs-lookup"><span data-stu-id="e200d-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="e200d-165">**CPU** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="e200d-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="e200d-166">**OSVersion** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="e200d-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="e200d-167">**Datei** =  _Pfad_</span><span class="sxs-lookup"><span data-stu-id="e200d-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="e200d-168">**VerknüpfungMit** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="e200d-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="e200d-169">**Registrierung** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="e200d-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="e200d-170">Im folgenden werden die beiden Beispiel **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="e200d-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="e200d-171">_Plattformzeichenfolge_ **]** Abschnitte, einen **Eintrag in der** Verwendung und mit den Eintrag **VerknüpfungMit** .</span><span class="sxs-lookup"><span data-stu-id="e200d-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="e200d-172">Die **[Plattform.**</span><span class="sxs-lookup"><span data-stu-id="e200d-172">The **[Platform.**</span></span> <span data-ttu-id="e200d-173">_Plattformzeichenfolge_ Abschnitt **]** wird ignoriert, wenn ein Formular in der lokalen Formularbibliothek hinzufügen, wenn angenommen wird, dass das Installationsprogramm hat die Dateien in den lokalen Speicher verfügbar den Message-Handler-Klasse darstellt, wie im Abschnitt in der OLE-Registrierung der Ereignishandler mit dem Namen, und wurde ausgeführt die OLE-Registrierung in der Registrierung des Systems.</span><span class="sxs-lookup"><span data-stu-id="e200d-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

