---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321735"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="ff547-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ff547-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="ff547-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff547-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff547-105">Ermöglicht Clientanwendungen den Zugriff auf Eigenschaften, die speziell für die Formulardefinition gelten.</span><span class="sxs-lookup"><span data-stu-id="ff547-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="ff547-106">Wenn Formular Informationen in einem separaten Objekt enthalten sind, kann der Formularbibliothek Anbieter ein Formular für einen Client ohne Aktivierung des Formulars beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ff547-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff547-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ff547-107">Header file:</span></span>  <br/> |<span data-ttu-id="ff547-108">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="ff547-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="ff547-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="ff547-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="ff547-110">Formular Informationsobjekte</span><span class="sxs-lookup"><span data-stu-id="ff547-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="ff547-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ff547-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff547-112">Formular Bibliotheks Anbieter</span><span class="sxs-lookup"><span data-stu-id="ff547-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="ff547-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ff547-113">Called by:</span></span>  <br/> |<span data-ttu-id="ff547-114">Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ff547-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="ff547-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="ff547-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ff547-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="ff547-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="ff547-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="ff547-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="ff547-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="ff547-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="ff547-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="ff547-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="ff547-120">Nicht durchgeführten</span><span class="sxs-lookup"><span data-stu-id="ff547-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ff547-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="ff547-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ff547-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="ff547-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="ff547-123">Gibt einen Zeiger auf den vollständigen Satz von Eigenschaften zurück, die ein Formular verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff547-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="ff547-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="ff547-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="ff547-125">Gibt einen Zeiger auf den vollständigen Satz von Verben zurück, die ein Formular verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff547-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="ff547-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="ff547-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="ff547-127">Erstellt ein Symbol aus einer Icon-Eigenschaft eines Formulars.</span><span class="sxs-lookup"><span data-stu-id="ff547-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="ff547-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="ff547-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="ff547-129">Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="ff547-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="ff547-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="ff547-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="ff547-131">Gibt einen Zeiger auf den Formular Container zurück, in dem ein bestimmtes Formular installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ff547-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff547-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff547-132">Remarks</span></span>

<span data-ttu-id="ff547-133">Im Gegensatz zu den meisten in der Headerdatei MapiForm. h definierten Schnittstellen erbt **IMAPIFormInfo** von der [IMAPIProp](imapipropiunknown.md) -Schnittstelle, da die meisten Formular Informationen über Aufrufe an die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff547-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff547-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff547-134">See also</span></span>



[<span data-ttu-id="ff547-135">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ff547-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

