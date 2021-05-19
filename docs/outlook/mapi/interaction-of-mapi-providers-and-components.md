---
title: Interaktion von MAPI-Anbietern und -Komponenten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434662"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="4c2f4-103">Interaktion von MAPI-Anbietern und -Komponenten</span><span class="sxs-lookup"><span data-stu-id="4c2f4-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="4c2f4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c2f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c2f4-105">MAPI-Dienstanbieter jeder Art müssen bestimmte Richtlinien befolgen, um mit anderen MAPI-Komponenten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="4c2f4-106">Jeder Dienstanbieter muss:</span><span class="sxs-lookup"><span data-stu-id="4c2f4-106">Each service provider must:</span></span>
  
- <span data-ttu-id="4c2f4-107">Verwenden Sie die richtigen Anbieter- und Anmeldeobjekte für die Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="4c2f4-108">Gibt bei der Initialisierung eine Verteilertabelle mit Anbietereintragspunkten an das Messagingsystem zurück.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="4c2f4-109">Registrieren Sie eine ZEILE der MAPI-Statustabelle für jede Ressource im Besitz des Anbieters, und rufen Sie die [IMAPISupport::ModifyStatusRow-Methode](imapisupport-modifystatusrow.md) zu entsprechenden Zeiten auf.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="4c2f4-110">Verwenden Sie [die IMAPISupport::NewUID-Methode,](imapisupport-newuid.md) um gültige eindeutige Bezeichner (UIDs) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="4c2f4-111">Unterstützt die gängigen MAPI-Schnittstellen für zurückgegebene Objekte.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="4c2f4-112">Verwenden Sie die MAPI-Speicherzuweisungsfunktionen, um Clientanwendungen zurückgegebenen Arbeitsspeicher zuzuordnen und von anderen Teilen des MAPI-Subsystems zugewiesenen Arbeitsspeicher frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="4c2f4-113">Verwalten Sie bei Bedarf einen Profilabschnitt, um Anmeldeinformationen im zugrunde liegenden Messagingsystem zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="4c2f4-114">Verwenden Sie [die IMAPISupport::RegisterPreprocessor-Methode,](imapisupport-registerpreprocessor.md) um alle Nachrichtenvorverarbeitungsfunktionen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="4c2f4-115">Fügen Sie die richtigen Headerdateien (einschließlich mapispi.h) ein, die allgemeine Konstanten, Strukturen, Schnittstellen und Rückgabewerte definieren.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="4c2f4-116">Befolgen Sie die Adressformatkonventionen für allgemeine Adresstypen.</span><span class="sxs-lookup"><span data-stu-id="4c2f4-116">Follow address format conventions for common address types.</span></span>
    

