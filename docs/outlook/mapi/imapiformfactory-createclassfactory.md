---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416076"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="e683f-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="e683f-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="e683f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e683f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e683f-105">Gibt ein Klassen factory-Objekt für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="e683f-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="e683f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e683f-106">Parameters</span></span>

 <span data-ttu-id="e683f-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="e683f-107">_clsidForm_</span></span>
  
> <span data-ttu-id="e683f-108">[in] Ein Klassenbezeichner für das Formular, das von der Klassen factory erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e683f-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="e683f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e683f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e683f-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="e683f-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e683f-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="e683f-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="e683f-112">[out] Ein Zeiger auf das Klassen factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e683f-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e683f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e683f-113">Return value</span></span>

<span data-ttu-id="e683f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e683f-114">S_OK</span></span> 
  
> <span data-ttu-id="e683f-115">Das Klassen factory-Objekt wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e683f-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e683f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e683f-116">Remarks</span></span>

<span data-ttu-id="e683f-117">Formularbetrachter rufen die **IMAPIFormFactory::CreateClassFactory-Methode** auf, um eine Klassen factory für ein bestimmtes Formular zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e683f-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="e683f-118">Die Klassen factory wird verwendet, um Instanzen eines Formulars zu erstellen, das Nachrichten einer bestimmten Klasse verarbeitet, und um den Zugriff auf diese Instanzen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e683f-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="e683f-119">Die **CreateClassFactory-Methode** wird von Formularanzeigen aufgerufen, um ein Klassen factory-Objekt für Formularserver zu erhalten, die mehrere Nachrichtenklassen implementieren.</span><span class="sxs-lookup"><span data-stu-id="e683f-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="e683f-120">Diese Methode empfängt eine Klassen-ID (CLSID) als Parameter.</span><span class="sxs-lookup"><span data-stu-id="e683f-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="e683f-121">Basierend auf diesem Parameter kann diese Methode die spezifische Art des zurückgebenden Klassen factory-Objekts bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e683f-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e683f-122">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e683f-122">Notes to implementers</span></span>

<span data-ttu-id="e683f-123">Sie können von Ihrer **CreateClassFactory-Implementierung** dasselbe Klassen factory-Objekt bei mehreren Aufrufen für denselben Klassenbezeichner zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e683f-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="e683f-124">Das Erstellen einer neuen Klassen factory-Instanz ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e683f-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="e683f-125">Sie können über eine einzelne Factoryimplementierung einer Klasse verfügen, mit der bei Bedarf geeignete Klassen factory-Instanzen oder mehrere Factoryimplementierungsklassen einer Klasse für jede Nachrichtenklasse erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e683f-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e683f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e683f-126">See also</span></span>



[<span data-ttu-id="e683f-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e683f-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

