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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2b2abf4440ee2d81a8e95dcdb5fde2daeaa6e6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575910"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="1ebfd-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1ebfd-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="1ebfd-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ebfd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ebfd-105">Ermöglicht den Client Applications Zugriff auf Eigenschaften, die speziell für Formulardefinition gelten.</span><span class="sxs-lookup"><span data-stu-id="1ebfd-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="1ebfd-106">Hält Formularinformationen in einem separaten Objekt, kann der Formular Bibliotheksanbieter ein Formulars an einen Client beschreiben, ohne das Formular aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1ebfd-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ebfd-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1ebfd-107">Header file:</span></span>  <br/> |<span data-ttu-id="1ebfd-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="1ebfd-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="1ebfd-109">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="1ebfd-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="1ebfd-110">Formular Informationen-Objekte</span><span class="sxs-lookup"><span data-stu-id="1ebfd-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="1ebfd-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1ebfd-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="1ebfd-112">Anbieter für Formular-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ebfd-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="1ebfd-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1ebfd-113">Called by:</span></span>  <br/> |<span data-ttu-id="1ebfd-114">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="1ebfd-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="1ebfd-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="1ebfd-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1ebfd-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="1ebfd-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="1ebfd-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="1ebfd-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="1ebfd-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="1ebfd-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="1ebfd-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="1ebfd-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="1ebfd-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="1ebfd-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1ebfd-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="1ebfd-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1ebfd-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="1ebfd-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="1ebfd-123">Gibt einen Zeiger auf den vollständigen Satz von Eigenschaften, die einem Formular verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ebfd-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="1ebfd-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="1ebfd-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="1ebfd-125">Gibt einen Zeiger auf den vollständigen Satz von Verben, die ein Formular verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1ebfd-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="1ebfd-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="1ebfd-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="1ebfd-127">Erstellt ein Symbol aus einer Icon-Eigenschaft eines Formulars an.</span><span class="sxs-lookup"><span data-stu-id="1ebfd-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="1ebfd-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="1ebfd-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="1ebfd-129">Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="1ebfd-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="1ebfd-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="1ebfd-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="1ebfd-131">Gibt einen Zeiger auf den Formular-Container, in dem ein bestimmtes Formular installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1ebfd-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ebfd-132">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="1ebfd-132">Remarks</span></span>

<span data-ttu-id="1ebfd-133">Im Gegensatz zu den meisten Schnittstellen in der Headerdatei MapiForm.h definiert erbt **IMAPIFormInfo** über die Benutzeroberfläche [IMAPIProp](imapipropiunknown.md) , da es die meisten Formularinformationen über Aufrufe der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode exportiert.</span><span class="sxs-lookup"><span data-stu-id="1ebfd-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ebfd-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ebfd-134">See also</span></span>



[<span data-ttu-id="1ebfd-135">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ebfd-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

