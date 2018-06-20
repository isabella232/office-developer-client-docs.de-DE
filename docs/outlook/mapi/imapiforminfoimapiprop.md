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
ms.openlocfilehash: fa439d0a6fa59bac787f09c3f894a750948a0a3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792164"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="83979-103">IMAPIFormInfo: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="83979-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="83979-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="83979-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="83979-105">Ermöglicht den Client Applications Zugriff auf Eigenschaften, die speziell für Formulardefinition gelten.</span><span class="sxs-lookup"><span data-stu-id="83979-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="83979-106">Hält Formularinformationen in einem separaten Objekt, kann der Formular Bibliotheksanbieter ein Formulars an einen Client beschreiben, ohne das Formular aktivieren.</span><span class="sxs-lookup"><span data-stu-id="83979-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="83979-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="83979-107">Header file:</span></span>  <br/> |<span data-ttu-id="83979-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="83979-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="83979-109">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="83979-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="83979-110">Formular Informationen-Objekte</span><span class="sxs-lookup"><span data-stu-id="83979-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="83979-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="83979-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="83979-112">Anbieter für Formular-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="83979-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="83979-113">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="83979-113">Called by:</span></span>  <br/> |<span data-ttu-id="83979-114">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="83979-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="83979-115">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="83979-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="83979-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="83979-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="83979-117">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="83979-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="83979-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="83979-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="83979-119">Transaktionsmodell:</span><span class="sxs-lookup"><span data-stu-id="83979-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="83979-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="83979-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="83979-121">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="83979-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="83979-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="83979-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="83979-123">Gibt einen Zeiger auf den vollständigen Satz von Eigenschaften, die einem Formular verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83979-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="83979-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="83979-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="83979-125">Gibt einen Zeiger auf den vollständigen Satz von Verben, die ein Formular verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83979-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="83979-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="83979-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="83979-127">Erstellt ein Symbol aus einer Icon-Eigenschaft eines Formulars an.</span><span class="sxs-lookup"><span data-stu-id="83979-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="83979-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="83979-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="83979-129">Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="83979-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="83979-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="83979-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="83979-131">Gibt einen Zeiger auf den Formular-Container, in dem ein bestimmtes Formular installiert ist.</span><span class="sxs-lookup"><span data-stu-id="83979-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83979-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="83979-132">Remarks</span></span>

<span data-ttu-id="83979-133">Im Gegensatz zu den meisten Schnittstellen in der Headerdatei MapiForm.h definiert erbt **IMAPIFormInfo** über die Benutzeroberfläche [IMAPIProp](imapipropiunknown.md) , da es die meisten Formularinformationen über Aufrufe der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode exportiert.</span><span class="sxs-lookup"><span data-stu-id="83979-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="83979-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83979-134">See also</span></span>



[<span data-ttu-id="83979-135">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="83979-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

