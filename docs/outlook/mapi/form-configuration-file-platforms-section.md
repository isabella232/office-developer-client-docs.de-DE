---
title: Abschnitt "Formular Konfigurationsdatei [Plattformen]"
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
# <a name="form-configuration-file-platforms-section"></a><span data-ttu-id="7d4c9-103">Abschnitt "Formular Konfigurationsdatei [Plattformen]"</span><span class="sxs-lookup"><span data-stu-id="7d4c9-103">Form Configuration File [Platforms] Section</span></span>

<span data-ttu-id="7d4c9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d4c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d4c9-105">Im Abschnitt **[Plattformen]** wird der vollständige Satz von Plattformen aufgelistet, die von diesem Formular unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-105">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="7d4c9-106">Jeder Platt Form Eintrag besteht aus der Präfix **Plattform.**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-106">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="7d4c9-107">_String_, wobei _String_ ein beliebiger Zeichenfolgen Code für die Plattform ist.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-107">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="7d4c9-108">Jede Zeichenfolge entspricht dem **CPU** -Eintrag eines einzelnen Abschnitts **[Plattformen]** .</span><span class="sxs-lookup"><span data-stu-id="7d4c9-108">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="7d4c9-109">Jeder Eintrag in einem Abschnitt **[Plattformen]** definiert eine _Plattformzeichenfolge_ , die auf eine nachfolgende **[Plattform verweist.**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-109">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="7d4c9-110">_Plattformzeichenfolge_ **]** -Abschnitt wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-110">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="7d4c9-111">Im Abschnitt **[Plattformen]** wird der vollständige Satz von Plattformen aufgelistet, die von diesem Formular unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-111">The **[Platforms]** section lists the complete set of platforms supported by this form.</span></span> <span data-ttu-id="7d4c9-112">Jeder Platt Form Eintrag besteht aus der Präfix **Plattform.**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-112">Each platform entry consists of the prefix **Platform.**</span></span> <span data-ttu-id="7d4c9-113">_String_, wobei _String_ ein beliebiger Zeichenfolgen Code für die Plattform ist.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-113">_string_, where  _string_ is an arbitrary string code for the platform.</span></span> <span data-ttu-id="7d4c9-114">Jede Zeichenfolge entspricht dem **CPU** -Eintrag eines einzelnen Abschnitts **[Plattformen]** .</span><span class="sxs-lookup"><span data-stu-id="7d4c9-114">Each string corresponds to the **CPU** entry of an individual **[Platforms]** sections.</span></span> <span data-ttu-id="7d4c9-115">Jeder Eintrag in einem Abschnitt **[Plattformen]** definiert eine _Plattformzeichenfolge_ , die auf eine nachfolgende **[Plattform verweist.**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-115">Each entry in a **[Platforms]** section defines a  _platform string_ that references a subsequent **[Platform.**</span></span> <span data-ttu-id="7d4c9-116">_Plattformzeichenfolge_ **]** -Abschnitt wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-116">_platform string_ **]** section as shown here.</span></span> 
  
<span data-ttu-id="7d4c9-117">**Plattformen**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-117">**[Platforms]**</span></span>
  
<span data-ttu-id="7d4c9-118">**Plattform**.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-118">**Platform**.</span></span> <span data-ttu-id="7d4c9-119">_Zeichenfolgen_ =  -_Plattformzeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="7d4c9-119">_string_ =  _platform string_</span></span>
  
<span data-ttu-id="7d4c9-120">Es folgt ein Beispiel für einen Abschnitt **[Plattformen]** .</span><span class="sxs-lookup"><span data-stu-id="7d4c9-120">Following is an example of a **[Platforms]** section.</span></span> 
  
```cpp
[Platforms]
Platform.1 = NTx86
Platform.2 = Win95

```

<span data-ttu-id="7d4c9-121">**[Platform.**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-121">Each **[Platform.**</span></span> <span data-ttu-id="7d4c9-122">_Plattformzeichenfolge_ **]** section enthält die beiden erforderlichen Einträge, **CPU** und **OSVersion**.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-122">_platform string_ **]** section contains the two required entries, **CPU** and **OSVersion**.</span></span> <span data-ttu-id="7d4c9-123">Der **CPU** -Eintrag gibt den Prozessor an, und der **OSVersion** -Eintrag gibt das Betriebssystem an.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-123">The **CPU** entry specifies the processor, and the **OSVersion** entry specifies the operating system.</span></span> <span data-ttu-id="7d4c9-124">Gültige **CPU** -Werte werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-124">Valid **CPU** values are described in the following table.</span></span> 
  
|<span data-ttu-id="7d4c9-125">**CPU-Eintrag**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-125">**CPU Entry**</span></span>|<span data-ttu-id="7d4c9-126">**Prozessor**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-126">**Processor**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d4c9-127">Ix86</span><span class="sxs-lookup"><span data-stu-id="7d4c9-127">Ix86</span></span>  <br/> |<span data-ttu-id="7d4c9-128">Prozessoren der Intel 80x86-und Pentium-Serie sowie äquivalente Prozessoren von AMD, Cyrix, NextGen und anderen Herstellern.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-128">Intel 80x86 and Pentium series processors, as well as equivalent processors from AMD, Cyrix, NextGen and other manufacturers.</span></span>  <br/> |
|<span data-ttu-id="7d4c9-129">MIPS</span><span class="sxs-lookup"><span data-stu-id="7d4c9-129">MIPS</span></span>  <br/> |<span data-ttu-id="7d4c9-130">MIPS-R4000 Series-Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-130">MIPS R4000 series processors.</span></span>  <br/> |
|<span data-ttu-id="7d4c9-131">AXP</span><span class="sxs-lookup"><span data-stu-id="7d4c9-131">AXP</span></span>  <br/> |<span data-ttu-id="7d4c9-132">Alpha-AXP-Prozessor für digitale Geräte Corporation.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-132">Digital Equipment Corporation Alpha AXP processor.</span></span>  <br/> |
|<span data-ttu-id="7d4c9-133">PPC</span><span class="sxs-lookup"><span data-stu-id="7d4c9-133">PPC</span></span>  <br/> |<span data-ttu-id="7d4c9-134">Motorola Power PC Series-Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-134">Motorola Power PC series processors.</span></span>  <br/> |
|<span data-ttu-id="7d4c9-135">M68</span><span class="sxs-lookup"><span data-stu-id="7d4c9-135">M68</span></span>  <br/> |<span data-ttu-id="7d4c9-136">Prozessoren der Mororola-68x00-Serie.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-136">Mororola 68x00 series processors.</span></span>  <br/> |
   
<span data-ttu-id="7d4c9-137">Gültige **OSVersion** -Werte werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-137">Valid **OSVersion** values are described in the following table.</span></span> 
  
|<span data-ttu-id="7d4c9-138">**OSVersion-Eintrag**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-138">**OSVersion Entry**</span></span>|<span data-ttu-id="7d4c9-139">**Betriebssystem**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-139">**Operating System**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d4c9-140">Win 3.1</span><span class="sxs-lookup"><span data-stu-id="7d4c9-140">Win3.1</span></span>  <br/> |<span data-ttu-id="7d4c9-141">Windows 3,1 und Windows für Workgroups 3,11.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-141">Windows 3.1 and Windows for Workgroups 3.11.</span></span>  <br/> |
|<span data-ttu-id="7d4c9-142">WinNT 3.5</span><span class="sxs-lookup"><span data-stu-id="7d4c9-142">WinNT3.5</span></span>  <br/> |<span data-ttu-id="7d4c9-143">Windows NT 3,5 oder niedriger.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-143">Windows NT 3.5 or lower.</span></span>  <br/> |
|<span data-ttu-id="7d4c9-144">Win95</span><span class="sxs-lookup"><span data-stu-id="7d4c9-144">Win95</span></span>  <br/> |<span data-ttu-id="7d4c9-145">Windows 95.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-145">Windows 95.</span></span>  <br/> |
|<span data-ttu-id="7d4c9-146">WinNT 4.0</span><span class="sxs-lookup"><span data-stu-id="7d4c9-146">WinNT4.0</span></span>  <br/> |<span data-ttu-id="7d4c9-147">Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-147">Windows NT 4.0.</span></span>  <br/> |
|<span data-ttu-id="7d4c9-148">Mac7</span><span class="sxs-lookup"><span data-stu-id="7d4c9-148">Mac7</span></span>  <br/> |<span data-ttu-id="7d4c9-149">Macintosh System 7.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-149">Macintosh System 7.</span></span>  <br/> |
   
<span data-ttu-id="7d4c9-150">Darüber hinaus wird die **[-Plattform.**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-150">Additionally, the **[Platform.**</span></span> <span data-ttu-id="7d4c9-151">_Plattformzeichenfolge_ **]** -Abschnitt muss entweder einen **Datei** -oder **LinkTo** -Eintrag enthalten.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-151">_platform string_ **]** section must contain either a **File** or **LinkTo** entry.</span></span> <span data-ttu-id="7d4c9-152">Der **Datei** Eintrag listet die ausführbare Datei der Formularserver Anwendung auf, die von der Formularbibliothek verwaltet und in ein neues Unterverzeichnis im Datenträgercache geladen wird, wenn das Formular gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-152">The **File** entry lists the form server application executable file that the form library maintains and loads into a new subdirectory in the disk cache when the form is launched.</span></span> <span data-ttu-id="7d4c9-153">Wenn stattdessen ein **LinkTo** -Eintrag verwendet wird, enthält er den Namen einer anderen Plattformzeichenfolge, von der die **Datei** Informationen entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-153">If a **LinkTo** entry is used instead, it contains the name of a different platform string from which the **File** information is taken.</span></span> <span data-ttu-id="7d4c9-154">Dies ist nützlich, wenn eine Version eines Formulars mehrere Plattformen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-154">This is useful if one version of a form supports multiple platforms.</span></span> 
  
<span data-ttu-id="7d4c9-155">Der **Registrierungs** Eintrag wird verwendet, wenn der **Datei** Eintrag verwendet wird, er identifiziert den Registrierungsschlüssel für die Formularbibliothek, in der die ausführbare Datei für die Formularserver Anwendung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-155">The **Registry** entry is used whenever the **File** entry is used, it identifies the registry key for the form library where the executable file for the form server application is stored.</span></span> <span data-ttu-id="7d4c9-156">Zeichenfolgen, denen ein umgekehrter Schrägstrich (\) vorangestellt wird, werden im Stammverzeichnis der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-156">Strings preceded by a backslash ( \ ) are placed at the root of the registry.</span></span> <span data-ttu-id="7d4c9-157">Zeichenfolgen, denen kein umgekehrter Schrägstrich vorangestellt wird, werden im HKEY_CLASSES_ROOT\CLSID\- _GUID_\-Registrierungsschlüssel gespeichert, wobei _GUID_ die **GUID** des Formulars ist.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-157">Strings not preceded by a backslash are placed in the HKEY_CLASSES_ROOT\CLSID\  _GUID_\ registry key, where  _GUID_ is the **GUID** of the form.</span></span> <span data-ttu-id="7d4c9-158">Die Zeichen "% d" können verwendet werden, um den Pfadnamen des Verzeichnisses anzugeben, aus dem die Formular Konfigurationsdatei gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-158">The characters "%d" can be used to indicate the pathname of the directory from which the form configuration file has been read.</span></span> <span data-ttu-id="7d4c9-159">Dies ist hilfreich, um andere Dateien mit Pfadnamen relativ zur Formular Konfigurationsdatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-159">This is useful for specifying other files with pathnames relative to the form configuration file.</span></span> <span data-ttu-id="7d4c9-160">**Mehrere Datei** -oder **Registrierungs** Einträge können mithilfe von File oder Registry als Präfix gefolgt von einem anderen Text angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-160">**Multiple File** or **Registry** entries can be specified by using File or Registry as a prefix followed by any other text.</span></span> <span data-ttu-id="7d4c9-161">Das Format für die **[-Plattform.**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-161">The format for the **[Platform.**</span></span> <span data-ttu-id="7d4c9-162">_Plattformzeichenfolge_ **]** section ist:</span><span class="sxs-lookup"><span data-stu-id="7d4c9-162">_platform string_ **]** section is:</span></span> 
  
- <span data-ttu-id="7d4c9-163">**Plattform.**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-163">**[Platform.**</span></span> <span data-ttu-id="7d4c9-164">_Plattformzeichenfolge_ **]**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-164">_platform string_ **]**</span></span>
    
- <span data-ttu-id="7d4c9-165">**CPU** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="7d4c9-165">**CPU** =  _string_</span></span>
    
- <span data-ttu-id="7d4c9-166">**OSVersion** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="7d4c9-166">**OSVersion** =  _string_</span></span>
    
- <span data-ttu-id="7d4c9-167">\*\*\*\* =  Dateipfad__</span><span class="sxs-lookup"><span data-stu-id="7d4c9-167">**File** =  _path_</span></span>
    
- <span data-ttu-id="7d4c9-168">**LinkTo** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="7d4c9-168">**LinkTo** =  _string_</span></span>
    
- <span data-ttu-id="7d4c9-169">**Registrierungs** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="7d4c9-169">**Registry** =  _string_</span></span>
  
<span data-ttu-id="7d4c9-170">Es folgen zwei Beispiele **[Platform.**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-170">The following are two example **[Platform.**</span></span> <span data-ttu-id="7d4c9-171">_Plattformzeichenfolge_ **]** Abschnitte, eine mit dem **Datei** Eintrag und einen mithilfe des **LinkTo** -Eintrags.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-171">_platform string_ **]** sections, one using the **File** entry and one using the **LinkTo** entry.</span></span> 
  
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

<span data-ttu-id="7d4c9-172">**[Platform.**</span><span class="sxs-lookup"><span data-stu-id="7d4c9-172">The **[Platform.**</span></span> <span data-ttu-id="7d4c9-173">_Plattformzeichenfolge_ **]** section wird beim Hinzufügen eines Formulars zur lokalen Formularbibliothek ignoriert, wenn davon ausgegangen wird, dass das Installationsprogramm die Dateien, die den Nachrichtenklassen Handler konstituieren, in verfügbaren lokalen Speicher, wie im Handler-Abschnitt in der OLE-Registrierung benannt, gespeichert hat und die OLE-Registrierung in der Systemregistrierung.</span><span class="sxs-lookup"><span data-stu-id="7d4c9-173">_platform string_ **]** section is ignored when adding a form to the local form library, when it is assumed that the installer has placed the files constituting the message class handler into available local storage as named in the handler's section in the OLE registry, and has done the OLE registration in the system's registry.</span></span> 
  

