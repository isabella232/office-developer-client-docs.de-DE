---
title: Interaktion von MAPI-Anbietern und-Komponenten
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
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="253b4-103">Interaktion von MAPI-Anbietern und-Komponenten</span><span class="sxs-lookup"><span data-stu-id="253b4-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="253b4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="253b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="253b4-105">MAPI-Dienstanbieter jeglicher Art müssen bestimmte Richtlinien befolgen, um mit anderen MAPI-Komponenten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="253b4-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="253b4-106">Jeder Dienstanbieter muss:</span><span class="sxs-lookup"><span data-stu-id="253b4-106">Each service provider must:</span></span>
  
- <span data-ttu-id="253b4-107">Verwenden Sie die richtigen Anbieter-und Anmeldeobjekte für die Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="253b4-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="253b4-108">Zurückgeben einer Dispatch-Tabelle mit Anbieter Einstiegspunkten nach der Initialisierung an das Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="253b4-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="253b4-109">Registrieren Sie eine MAPI-Statustabellen Zeile für jede Ressource, die im Besitz des Anbieters ist, und rufen Sie die [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode zu geeigneten Zeiten auf.</span><span class="sxs-lookup"><span data-stu-id="253b4-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="253b4-110">Verwenden Sie die [IMAPISupport:: NewUID](imapisupport-newuid.md) -Methode, um gültige eindeutige IDs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="253b4-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="253b4-111">Unterstützen der allgemeinen MAPI-Schnittstellen für Objekte, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="253b4-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="253b4-112">Verwenden Sie die MAPI-Speicher Zuweisungsfunktionen, um an Clientanwendungen zurückgegebener Speicher zuzuweisen und den von anderen Teilen des MAPI-Subsystems reservierten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="253b4-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="253b4-113">Führen Sie bei Bedarf einen Profil Abschnitt aus, um die Anmeldeinformationen für das zugrunde liegende Messagingsystem zu speichern.</span><span class="sxs-lookup"><span data-stu-id="253b4-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="253b4-114">Verwenden Sie die [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode, um alle Funktionen der Nachrichten Vorverarbeitung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="253b4-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="253b4-115">Schließen Sie die richtigen Headerdateien (einschließlich mapispi. h) ein, die allgemeine Konstanten, Strukturen, Schnittstellen und Rückgabewerte definieren.</span><span class="sxs-lookup"><span data-stu-id="253b4-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="253b4-116">BeFolgen Sie die Adressformat Konventionen für allgemeine Adresstypen.</span><span class="sxs-lookup"><span data-stu-id="253b4-116">Follow address format conventions for common address types.</span></span>
    

