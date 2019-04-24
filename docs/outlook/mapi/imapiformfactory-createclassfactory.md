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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342175"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="8dec8-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="8dec8-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="8dec8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dec8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dec8-105">Gibt ein klassenfactoryobjekt für das Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="8dec8-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="8dec8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8dec8-106">Parameters</span></span>

 <span data-ttu-id="8dec8-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="8dec8-107">_clsidForm_</span></span>
  
> <span data-ttu-id="8dec8-108">in Ein Klassenbezeichner für das Formular, das von der Klassenfactory erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8dec8-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="8dec8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8dec8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8dec8-110">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="8dec8-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8dec8-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="8dec8-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="8dec8-112">Out Ein Zeiger auf das Klassenfactory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8dec8-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8dec8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8dec8-113">Return value</span></span>

<span data-ttu-id="8dec8-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="8dec8-114">S_OK</span></span> 
  
> <span data-ttu-id="8dec8-115">Das Klassenfactory-Objekt wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8dec8-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8dec8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8dec8-116">Remarks</span></span>

<span data-ttu-id="8dec8-117">Formular Betrachter rufen die **IMAPIFormFactory:: CreateClassFactory** -Methode auf, um eine Klassenfactory für ein bestimmtes Formular abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8dec8-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="8dec8-118">Die Class Factory wird verwendet, um Instanzen eines Formulars zu erstellen, das Nachrichten einer bestimmten Klasse verarbeitet und den Zugriff auf diese Instanzen steuert.</span><span class="sxs-lookup"><span data-stu-id="8dec8-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="8dec8-119">Die **CreateClassFactory** -Methode wird von Formular Viewern aufgerufen, um ein klassenfactoryobjekt für Formularserver abzurufen, die mehrere Nachrichtenklassen implementieren.</span><span class="sxs-lookup"><span data-stu-id="8dec8-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="8dec8-120">Diese Methode empfängt eine Klassen-ID (CLSID) als Parameter.</span><span class="sxs-lookup"><span data-stu-id="8dec8-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="8dec8-121">Anhand dieses Parameters kann diese Methode die spezifische Art des zurückzugebenden Klassenfactory-Objekts bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8dec8-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8dec8-122">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="8dec8-122">Notes to implementers</span></span>

<span data-ttu-id="8dec8-123">Sie können von der **CreateClassFactory** -Implementierung das gleiche Klassenfactory-Objekt für mehrere Aufrufe für denselben Klassenbezeichner zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8dec8-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="8dec8-124">Das Erstellen einer neuen Klassenfactory-Instanz ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8dec8-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="8dec8-125">Sie können eine einzelne Klasse Factory-Implementierung haben, die entsprechende Klassen Factory-Instanzen bei Bedarf erstellt, oder mehrere Klassenfactory-Implementierungen, eine für jede Nachrichtenklasse.</span><span class="sxs-lookup"><span data-stu-id="8dec8-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8dec8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dec8-126">See also</span></span>



[<span data-ttu-id="8dec8-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8dec8-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

