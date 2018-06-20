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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 823e10a1f496f5f5e8bab00f94d700d06e753b48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792170"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="d6274-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="d6274-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="d6274-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6274-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6274-105">Gibt ein Klasse Factory-Objekt für das Formular.</span><span class="sxs-lookup"><span data-stu-id="d6274-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="d6274-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6274-106">Parameters</span></span>

 <span data-ttu-id="d6274-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="d6274-107">_clsidForm_</span></span>
  
> <span data-ttu-id="d6274-108">[in] Eine Klassen-ID für das Formular von der Klassenfactory erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6274-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="d6274-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6274-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d6274-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="d6274-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d6274-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="d6274-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="d6274-112">[out] Ein Zeiger auf das Klassenobjekt Factory.</span><span class="sxs-lookup"><span data-stu-id="d6274-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6274-113">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d6274-113">Return value</span></span>

<span data-ttu-id="d6274-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6274-114">S_OK</span></span> 
  
> <span data-ttu-id="d6274-115">Das Klassenobjekt Factory wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6274-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6274-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d6274-116">Remarks</span></span>

<span data-ttu-id="d6274-117">Formular Viewer rufen Sie die **IMAPIFormFactory::CreateClassFactory** -Methode, um eine Klassenfactory für ein bestimmtes Formular zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d6274-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="d6274-118">Die ClassFactory wird verwendet, um Instanzen eines Formulars zu erstellen, die Nachrichten von einer bestimmten Klasse behandelt und den Zugriff auf diese Instanzen steuern.</span><span class="sxs-lookup"><span data-stu-id="d6274-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="d6274-119">Die **CreateClassFactory** -Methode wird von Formular Zuschauer zu einer Factory Klassenobjekt für Formular-Server abzurufen, die mehrere Nachrichtenklassen implementieren aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d6274-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="d6274-120">Diese Methode empfängt eine Klassen-ID (CLSID) als Parameter.</span><span class="sxs-lookup"><span data-stu-id="d6274-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="d6274-121">Basierend auf diesen Parameter, kann diese Methode die Art des zurückzugebenden Klassenfactoryobjekts-Factory bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d6274-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d6274-122">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d6274-122">Notes to implementers</span></span>

<span data-ttu-id="d6274-123">Sie können aus der **CreateClassFactory** -Implementierung das gleiche Factory Klassenobjekt auf mehrere Aufrufe für die gleichen Klassen-ID zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d6274-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="d6274-124">Erstellen einer neuen Instanz der Klasse Factory ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6274-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="d6274-125">Sie können eine einzelne Klasse Factory-Implementierung, die Instanzen der entsprechenden Factory bei Bedarf erstellt oder mehrere Klasse Factory Implementierungen für jede Nachrichtenklasse haben.</span><span class="sxs-lookup"><span data-stu-id="d6274-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6274-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6274-126">See also</span></span>



[<span data-ttu-id="d6274-127">IMAPIFormFactory: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6274-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

