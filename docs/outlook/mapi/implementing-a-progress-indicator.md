---
title: Implementieren eine Statusanzeige
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 767b8723d9a544a31ee5c4bbc1d6186a15387b44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792538"
---
# <a name="implementing-a-progress-indicator"></a><span data-ttu-id="ca1ba-103">Implementieren eine Statusanzeige</span><span class="sxs-lookup"><span data-stu-id="ca1ba-103">Implementing a Progress Indicator</span></span>

  
  
<span data-ttu-id="ca1ba-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca1ba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca1ba-105">Viele Vorgänge, die von Clients initiiert beanspruchen sehr viel Zeit.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-105">Many of the operations initiated by clients take a significant amount of time.</span></span> <span data-ttu-id="ca1ba-106">Einer der Eingabeparameter für diese Vorgänge potenziell langen ist ein Zeiger auf ein Objekt Fortschritt – ein Objekt, das implementiert die [IMAPIProgress: IUnknown](imapiprogressiunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-106">One of the input parameters to these potentially lengthy operations is a pointer to a progress object — an object that implements the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface.</span></span> <span data-ttu-id="ca1ba-107">Fortschritt Objekte Steuern der Darstellung und Anzeige von Statusanzeigen und von Clients und von MAPI implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-107">Progress objects control the appearance and display of progress indicators and are implemented by clients and by MAPI.</span></span> <span data-ttu-id="ca1ba-108">Sie können auswählen, ob einem Fortschritt-Objekt implementiert werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-108">You can choose whether or not to implement a progress object.</span></span> <span data-ttu-id="ca1ba-109">Die MAPI-Implementierung ist verfügbar für Dienstanbieter zu verwenden, wenn Sie festlegen, dass keine Implementierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-109">The MAPI implementation is available for service providers to use if you elect not to supply an implementation.</span></span> 
  
<span data-ttu-id="ca1ba-110">Fortschritt Objekte arbeiten Sie mit der folgenden Datenelemente:</span><span class="sxs-lookup"><span data-stu-id="ca1ba-110">Progress objects work with the following pieces of data:</span></span>
  
- <span data-ttu-id="ca1ba-111">Eine globale Mindestwert, der Ihre [IMAPIProgress::Progress](imapiprogress-progress.md) -Methode aufgerufen wird, kleiner oder gleich dem Wert des Parameters _UlValue_ sein sollte.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-111">A global minimum value which, when your [IMAPIProgress::Progress](imapiprogress-progress.md) method is called, should be less than or equal to the value of the  _ulValue_ parameter.</span></span> <span data-ttu-id="ca1ba-112">Am Anfang des Vorgangs werden diese Minimalwert _UlValue_ .</span><span class="sxs-lookup"><span data-stu-id="ca1ba-112">At the beginning of the operation,  _ulValue_ will be equal to this minimum value.</span></span> 
    
- <span data-ttu-id="ca1ba-113">Einen globalen maximale Wert, der die **IMAPIProgress::Progress** -Methode aufgerufen wird, größer als oder gleich dem Parameter _UlValue_ sein sollte.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-113">A global maximum value which, when your **IMAPIProgress::Progress** method is called, should be greater than or equal to the  _ulValue_ parameter.</span></span> <span data-ttu-id="ca1ba-114">Am Ende des Vorgangs werden diese Maximalwert _UlValue_ .</span><span class="sxs-lookup"><span data-stu-id="ca1ba-114">At the end of the operation,  _ulValue_ will be equal to this maximum value.</span></span> 
    
- <span data-ttu-id="ca1ba-115">Ein Kennzeichen Wert gibt an, ob der Status von oben entspricht oder niedrigerer Ebene item.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-115">A flags value which indicates whether the progress corresponds to a top or lower level item.</span></span>
    
- <span data-ttu-id="ca1ba-116">Ein Wert, der angibt, die aktuelle Stufe des Fortschritt für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-116">A value that indicates the current level of progress for the operation.</span></span>
    
- <span data-ttu-id="ca1ba-117">Die Anzahl der derzeit verarbeiteten Elemente relativ zur Summe.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-117">The number of the currently processed items relative to the total.</span></span>
    
- <span data-ttu-id="ca1ba-118">Die Gesamtanzahl von Elementen, die während des Vorgangs verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-118">The total number of items to be processed during the operation.</span></span>
    
<span data-ttu-id="ca1ba-119">Die minimale und maximale Werte darstellen Anfang und Ende des Vorgangs in numerische Form.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-119">The minimum and maximum values represent the beginning and end of the operation in numeric form.</span></span> <span data-ttu-id="ca1ba-120">Verwenden Sie 1 für die anfängliche Mindestwert und 1000 Höchstwert für die anfängliche, diese Werte in den Methoden [IMAPIProgress::GetMin](imapiprogress-getmin.md) und [IMAPIProgress::GetMax](imapiprogress-getmax.md) Dienstanbietern übergeben.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-120">Use 1 for the initial minimum value and 1000 for the initial maximum value, passing these values to service providers in the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods.</span></span> <span data-ttu-id="ca1ba-121">Dienstanbieter setzen Sie diese Werte beim Aufruf von [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-121">Service providers reset these values when they call [IMAPIProgress::SetLimits](imapiprogress-setlimits.md).</span></span> 
  
<span data-ttu-id="ca1ba-122">Der Wert des Flags wird vom Dienstanbieter verwendet, um zu bestimmen, wie sie die anderen Werte festlegen sollten.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-122">The flags value is used by service providers to determine how they should set the other values.</span></span> <span data-ttu-id="ca1ba-123">Den Wert des Flags auf MAPI_TOP_LEVEL zu initialisieren und Rückgabewert dieses in die Implementierung von **"GetFlags"** , bis der Dienstanbieter durch Aufrufen von **SetLimits**zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-123">Initialize the flags value to MAPI_TOP_LEVEL and return this value in your implementation of **GetFlags** until the service provider resets it by calling **SetLimits**.</span></span> 
  
<span data-ttu-id="ca1ba-124">Speichern Sie lokale Kopien der einzelnen Parameter in der Implementierung der **SetLimits** -Methode: _LpulMin_, _LpulMax_und _LpulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-124">In your implementation of the **SetLimits** method, save local copies of each of the parameters:  _lpulMin_,  _lpulMax_, and  _lpulFlags_.</span></span> <span data-ttu-id="ca1ba-125">Diese Werte sollten sofort verfügbar sein, bei ein Dienstanbieter Ihrer **GetMin**, **GetMax**oder **"GetFlags"** aufruft.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-125">These values should be readily available when a service provider calls your **GetMin**, **GetMax**, or **GetFlags** methods.</span></span> 
  
<span data-ttu-id="ca1ba-126">Dienstanbieter Aufrufen **IMAPIProgress::Progress** Methode, um die Anzeige der Statusanzeige zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-126">To update the display of the progress indicator, service providers call your **IMAPIProgress::Progress** method.</span></span> <span data-ttu-id="ca1ba-127">Es gibt drei Parameter an diese Methode: ein Wert, der die Anzahl und insgesamt.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-127">There are three parameters to this method: a value, a count, and a total.</span></span> <span data-ttu-id="ca1ba-128">Verwenden Sie den ersten Parameter _UlValue_, um die Statusanzeige anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-128">Use the first parameter,  _ulValue_, to display the progress indicator.</span></span> <span data-ttu-id="ca1ba-129">Der Parameter _UlValue_ wird die Statusanzeige und werden nur globale _UlMin_ am Anfang des Vorgangs gleich und gleich globale _UlMax_ nur nach Abschluss des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-129">The  _ulValue_ parameter is the progress indicator and will be equal to global  _ulMin_ only at the very beginning of the operation and equal to global  _ulMax_ only at the completion of the operation.</span></span> 
  
<span data-ttu-id="ca1ba-130">Verwenden Sie die zweite und dritte Parameter sowie die _UlCount_ und _UlTotal_, falls verfügbar, um eine optionale Nachricht wie "5 Elemente nicht genügend 10 abgeschlossen." angezeigt</span><span class="sxs-lookup"><span data-stu-id="ca1ba-130">Use the second and third parameters,  _ulCount_ and  _ulTotal_, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="ca1ba-131">Wenn die zweite und dritte Parameter auf 0 festgelegt sind, können Sie, ob er die Statusanzeige visuell zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-131">If the second and third parameters are set to 0, you can choose whether or not to visually change the progress indicator.</span></span> <span data-ttu-id="ca1ba-132">Einige Dienstanbieter legen Sie diesen Parameter auf Nullen, um anzugeben, dass sie ein Unterobjekt verarbeitet werden, deren Status relativ zu einem übergeordneten Objekt überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-132">Some service providers set these parameters to zeroes to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="ca1ba-133">In diesem Fall ist es sinnvoll, die Anzeige nur ändern, wenn das übergeordnete Objekt des Fortschritts meldet.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-133">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="ca1ba-134">Einige Dienstanbieter übergeben Nullen für diese Parameter jedes Mal.</span><span class="sxs-lookup"><span data-stu-id="ca1ba-134">Some service providers pass zeroes for these parameters every time.</span></span> 
  
