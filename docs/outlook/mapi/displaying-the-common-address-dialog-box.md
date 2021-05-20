---
title: Anzeigen des Dialogfelds "Allgemeine Adresse"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436903"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="22a2b-103">Anzeigen des Dialogfelds "Allgemeine Adresse"</span><span class="sxs-lookup"><span data-stu-id="22a2b-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="22a2b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22a2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22a2b-105">Das Dialogfeld allgemeine MAPI-Adresse kann für eine Vielzahl von Adressierungsaufgaben verwendet werden, z. B. das Erstellen einer Empfängerliste.</span><span class="sxs-lookup"><span data-stu-id="22a2b-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="22a2b-106">Rufen Sie zum Anzeigen dieses Dialogfelds **IAddrBook::Address auf.**</span><span class="sxs-lookup"><span data-stu-id="22a2b-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="22a2b-107">Je nachdem, welche der vielen Parameter Sie festlegen und wie Sie sie festlegen, können Sie die Anzeige auf Einträge eines bestimmten Typs aus einem bestimmten Container beschränken.</span><span class="sxs-lookup"><span data-stu-id="22a2b-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="22a2b-108">**So beschränken Sie das Adressdialogfeld auf die Anzeige von Einträgen im persönlichen Adressbuch (PAB)**</span><span class="sxs-lookup"><span data-stu-id="22a2b-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="22a2b-109">Rufen [Sie IAddrBook::GetPAB auf,](iaddrbook-getpab.md) um die Eintrags-ID des PAB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="22a2b-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="22a2b-110">Erstellen Sie eine Eigenschaftseinschränkung, die RELOP_EQ für das **#A0** der [SPropertyRestriction-Struktur](spropertyrestriction.md) und **entweder PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) als **ulPropTag-Element** verwendet.</span><span class="sxs-lookup"><span data-stu-id="22a2b-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="22a2b-111">Wenn Sie **PR_ENTRYID** verwenden, übergeben Sie den eintragsbezeichner, der aus **GetPAB abgerufen wurde.**</span><span class="sxs-lookup"><span data-stu-id="22a2b-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="22a2b-112">Wenn Sie **PR_AB_PROVIDER_ID** verwenden, übergeben Sie den im MSPAB enthaltenen Wert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="22a2b-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="22a2b-113">**PR_AB_PROVIDER_ID** ist der eindeutige Bezeichner für das von MAPI entworfene PAB.</span><span class="sxs-lookup"><span data-stu-id="22a2b-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="22a2b-114">Rufen [Sie IAddrBook::Address auf,](iaddrbook-address.md) mit dem  _lpHierRestriction-Parameter,_ der auf die Eigenschaftseinschränkung verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="22a2b-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

