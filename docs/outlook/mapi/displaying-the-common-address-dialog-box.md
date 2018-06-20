---
title: Das Dialogfeld allgemeine Adresse anzuzeigen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7b603504956be9ec3066e5ff5e1d5db7d59852a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791584"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="6c3ae-103">Das Dialogfeld allgemeine Adresse anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="6c3ae-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="6c3ae-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c3ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c3ae-105">MAPI-Adresse im allgemeinen Dialogfeld kann für eine Vielzahl von Adressierung Aufgaben wie das Erstellen einer Empfängerliste verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c3ae-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="6c3ae-106">Rufen Sie **IAddrBook::Address**, um das Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6c3ae-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="6c3ae-107">Je nachdem, welches der viele Parameter, die Sie festlegen und wie Sie festlegen, können Sie die Anzeige von einem bestimmten Container den Einträgen eines bestimmten Typs einschränken.</span><span class="sxs-lookup"><span data-stu-id="6c3ae-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="6c3ae-108">**Um das Dialogfeld Adresse zum Anzeigen von persönlichen (PAB) Adressbucheinträge nur zu begrenzen**</span><span class="sxs-lookup"><span data-stu-id="6c3ae-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="6c3ae-109">Rufen Sie [IAddrBook::GetPAB](iaddrbook-getpab.md) , um die Eintrags-ID des PAB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6c3ae-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="6c3ae-110">Erstellen Sie eine eigenschaftseinschränkung, die für die **relop** Mitglied der [SPropertyRestriction](spropertyrestriction.md) -Struktur und entweder **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) oder **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) RELOP_EQ verwendet als die **UlPropTag** Member.</span><span class="sxs-lookup"><span data-stu-id="6c3ae-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="6c3ae-111">Wenn Sie **PR_ENTRYID**verwenden, übergeben Sie die Eintrags-ID von **GetPAB**abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6c3ae-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="6c3ae-112">Wenn Sie **PR_AB_PROVIDER_ID**verwenden, übergeben Sie den Wert in der MSPAB enthalten. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="6c3ae-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="6c3ae-113">**PR_AB_PROVIDER_ID** ist der eindeutige Bezeichner für die PAB durch MAPI vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="6c3ae-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="6c3ae-114">Rufen Sie [IAddrBook::Address](iaddrbook-address.md) mit dem _LpHierRestriction_ -Parameter auf der eigenschaftseinschränkung zeigen.</span><span class="sxs-lookup"><span data-stu-id="6c3ae-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    
