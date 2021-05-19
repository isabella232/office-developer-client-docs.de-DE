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
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417364"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="13216-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="13216-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="13216-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13216-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13216-105">Ermöglicht Clientanwendungen Zugriff auf Eigenschaften, die für die Formulardefinition besonders sind.</span><span class="sxs-lookup"><span data-stu-id="13216-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="13216-106">Wenn Formularinformationen in einem separaten Objekt gespeichert werden, kann der Formularbibliotheksanbieter ein Formular für einen Client beschreiben, ohne das Formular zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="13216-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13216-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="13216-107">Header file:</span></span>  <br/> |<span data-ttu-id="13216-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="13216-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="13216-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="13216-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="13216-110">Formularinformationsobjekte</span><span class="sxs-lookup"><span data-stu-id="13216-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="13216-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="13216-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="13216-112">Anbieter von Formularbibliotheken</span><span class="sxs-lookup"><span data-stu-id="13216-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="13216-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="13216-113">Called by:</span></span>  <br/> |<span data-ttu-id="13216-114">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="13216-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="13216-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="13216-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="13216-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="13216-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="13216-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="13216-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="13216-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="13216-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="13216-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="13216-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="13216-120">Nichttransaktioniert</span><span class="sxs-lookup"><span data-stu-id="13216-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="13216-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="13216-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="13216-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="13216-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="13216-123">Gibt einen Zeiger auf den vollständigen Satz von Eigenschaften zurück, den ein Formular verwendet.</span><span class="sxs-lookup"><span data-stu-id="13216-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="13216-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="13216-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="13216-125">Gibt einen Zeiger auf den vollständigen Satz von Verben zurück, den ein Formular verwendet.</span><span class="sxs-lookup"><span data-stu-id="13216-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="13216-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="13216-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="13216-127">Erstellt ein Symbol aus einer Icon-Eigenschaft eines Formulars.</span><span class="sxs-lookup"><span data-stu-id="13216-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="13216-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="13216-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="13216-129">Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="13216-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="13216-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="13216-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="13216-131">Gibt einen Zeiger auf den Formularcontainer zurück, in dem ein bestimmtes Formular installiert ist.</span><span class="sxs-lookup"><span data-stu-id="13216-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13216-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13216-132">Remarks</span></span>

<span data-ttu-id="13216-133">Im Gegensatz zu den meisten in der MapiForm.h-Headerdatei definierten Schnittstellen erbt **IMAPIFormInfo** von der [IMAPIProp-Schnittstelle,](imapipropiunknown.md) da die meisten Formularinformationen über Aufrufe der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="13216-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13216-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13216-134">See also</span></span>



[<span data-ttu-id="13216-135">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="13216-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

