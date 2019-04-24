---
title: Anzeigen des Dialog Felds "allgemeine Adresse"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337093"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="2420a-103">Anzeigen des Dialog Felds "allgemeine Adresse"</span><span class="sxs-lookup"><span data-stu-id="2420a-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="2420a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2420a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2420a-105">Das Dialogfeld MAPI-allgemeine Adresse kann für eine Vielzahl von Adressierungs Aufgaben wie das Erstellen einer Empfängerliste verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2420a-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="2420a-106">Um dieses Dialogfeld anzuzeigen, rufen Sie **IAddrBook:: Address**auf.</span><span class="sxs-lookup"><span data-stu-id="2420a-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="2420a-107">Je nachdem, welche Zahl von Parametern Sie festlegen und wie Sie Sie festlegen, können Sie die Anzeige auf Einträge eines bestimmten Typs von einem bestimmten Container beschränken.</span><span class="sxs-lookup"><span data-stu-id="2420a-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="2420a-108">**So begrenzen Sie das Dialogfeld "Adresse" auf die Anzeige von persönlichen Adressbucheinträgen (PAB)**</span><span class="sxs-lookup"><span data-stu-id="2420a-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="2420a-109">Rufen Sie [IAddrBook:: GetPAB](iaddrbook-getpab.md) auf, um den Eintragsbezeichner des PAB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2420a-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="2420a-110">Erstellen Sie eine Eigenschaftseinschränkung, die RELOP_EQ für das **RELOP** -Element der [SPropertyRestriction](spropertyrestriction.md) -Struktur verwendet, und entweder **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_AB_PROVIDER_ID** ([pidtagabproviderid (](pidtagabproviderid-canonical-property.md)) als **ulPropTag** -Element.</span><span class="sxs-lookup"><span data-stu-id="2420a-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="2420a-111">Wenn Sie **PR_ENTRYID**verwenden, müssen Sie die Eintrags-ID von **GetPAB**.</span><span class="sxs-lookup"><span data-stu-id="2420a-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="2420a-112">Wenn Sie **PR_AB_PROVIDER_ID**verwenden, müssen Sie den in der MSPAB enthaltenen Wert überschreiten. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="2420a-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="2420a-113">**PR_AB_PROVIDER_ID** ist der eindeutige Bezeichner für das von MAPI entwickelte PAB.</span><span class="sxs-lookup"><span data-stu-id="2420a-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="2420a-114">Rufen Sie [IAddrBook:: Address](iaddrbook-address.md) mit dem _lpHierRestriction_ -Parameter auf, der auf die Eigenschaftseinschränkung zeigt.</span><span class="sxs-lookup"><span data-stu-id="2420a-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

