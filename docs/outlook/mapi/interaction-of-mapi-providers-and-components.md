---
title: Interaktion von MAPI-Anbietern und Komponenten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cb0f8d5077b4851a50ceb8523943ae760a8ee5ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792721"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="73218-103">Interaktion von MAPI-Anbietern und Komponenten</span><span class="sxs-lookup"><span data-stu-id="73218-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="73218-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73218-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73218-105">MAPI-Dienstanbieter jeglicher Art müssen bestimmte Richtlinien andere MAPI-Komponenten entwickelt.</span><span class="sxs-lookup"><span data-stu-id="73218-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="73218-106">Jeder Dienstanbieter muss:</span><span class="sxs-lookup"><span data-stu-id="73218-106">Each service provider must:</span></span>
  
- <span data-ttu-id="73218-107">Verwenden Sie die entsprechenden Objekte Anbieter und die Anmeldeinformationen für die Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="73218-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="73218-108">Zurückgeben einer Tabelle Versendung der Anbieter Einstiegspunkte an die messaging-System bei der Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="73218-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="73218-109">Registrieren Sie eine MAPI-Status Tabellenzeile für jede Ressource, die vom Anbieter gehören, und rufen Sie die [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode zum entsprechenden Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="73218-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="73218-110">Verwenden Sie die [IMAPISupport::NewUID](imapisupport-newuid.md) -Methode, um gültige eindeutige Bezeichner (UIDs) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="73218-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="73218-111">Unterstützt die gemeinsamen MAPI-Schnittstellen für Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="73218-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="73218-112">Verwenden Sie die MAPI-Speicherverwaltungsfunktionen Speicher Clientanwendungen zurückgegeben und durch andere Teile des MAPI-Subsystems Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="73218-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="73218-113">Verwalten eines Abschnitts Profil; bei Bedarf zum Speichern von Anmeldeinformationen für den zugrunde liegenden messaging-System.</span><span class="sxs-lookup"><span data-stu-id="73218-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="73218-114">Verwenden Sie die [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode, um eine beliebige Nachricht vorverarbeitung Funktionen registrieren.</span><span class="sxs-lookup"><span data-stu-id="73218-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="73218-115">Einfügen der richtigen Headerdateien (einschließlich mapispi.h), die definieren, häufige Konstanten, Strukturen, Schnittstellen und Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="73218-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="73218-116">Führen Sie die Adresse Format Konventionen für allgemeine Adresstypen.</span><span class="sxs-lookup"><span data-stu-id="73218-116">Follow address format conventions for common address types.</span></span>
    

