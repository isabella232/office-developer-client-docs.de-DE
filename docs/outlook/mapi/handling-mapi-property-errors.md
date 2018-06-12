---
title: Fehlerbehandlung von MAPI-Eigenschaft
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bb001d159141f70e9a82fa533e805f2a96b230ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791797"
---
# <a name="handling-mapi-property-errors"></a><span data-ttu-id="1eab5-103">Fehlerbehandlung von MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1eab5-103">Handling MAPI property errors</span></span>

<span data-ttu-id="1eab5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1eab5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1eab5-105">Anstatt vollst�ndige Fehler oder Erfolg melden die folgenden Methoden **IMAPIProp** partiellen Erfolg:</span><span class="sxs-lookup"><span data-stu-id="1eab5-105">Instead of complete failure or success, the following **IMAPIProp** methods report partial success:</span></span> 
  
[<span data-ttu-id="1eab5-106">GetProps</span><span class="sxs-lookup"><span data-stu-id="1eab5-106">GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="1eab5-107">SetProps</span><span class="sxs-lookup"><span data-stu-id="1eab5-107">SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="1eab5-108">"DeleteProps"</span><span class="sxs-lookup"><span data-stu-id="1eab5-108">DeleteProps</span></span>](imapiprop-deleteprops.md)
  
[<span data-ttu-id="1eab5-109">CopyTo</span><span class="sxs-lookup"><span data-stu-id="1eab5-109">CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="1eab5-110">CopyProps</span><span class="sxs-lookup"><span data-stu-id="1eab5-110">CopyProps</span></span>](imapiprop-copyprops.md)
  
<span data-ttu-id="1eab5-p101">**GetProps** partiellen Erfolg meldet, wenn mindestens eine der angeforderten Eigenschaften f�r ein Objekt abgerufen werden kann. **GetProps** gibt partiellen Erfolg an, indem die Warnung MAPI_W_ERRORS_RETURNED zur�ckgeben und Informationen zu den Eigenschaften nicht verf�gbar in den Wert-Array-Eigenschaft auf die durch den Parameter **lppPropArray**. Eine nicht verf�gbar-Eigenschaft Eintrag in diesem Array enth�lt PT_ERROR f�r den Eigenschaftentyp den **ulPropTag** Member und MAPI_E_NOT_FOUND oder einem anderen geeigneten Fehlerwert f�r den **Value** -Member. Beispielsweise platziert, wenn ein Client einen Ordner **GetProps** -Methode zum Abrufen von drei Eigenschaften aufruft, und die dritte nicht verf�gbar ist, der Nachricht Informationsdienst PT_ERROR in der dritten Eigenschaftstyp in Array der Wert-Eigenschaft und MAPI_E_NOT_FOUND im dritten-Eigenschaftenwert.</span><span class="sxs-lookup"><span data-stu-id="1eab5-p101">**GetProps** reports partial success when it can retrieve at least one of the requested properties for an object. **GetProps** indicates partial success by returning the warning MAPI_W_ERRORS_RETURNED and placing information about the unavailable properties in the property value array pointed to by the **lppPropArray** parameter. An unavailable property's entry in this array contains PT_ERROR for the property type in the **ulPropTag** member and MAPI_E_NOT_FOUND or another appropriate error value for the **Value** member. For example, if a client calls a folder's **GetProps** method to retrieve three properties and the third is unavailable, the message store provider places PT_ERROR in the third property type in the property value array and MAPI_E_NOT_FOUND in the third property value.</span></span> 
  
<span data-ttu-id="1eab5-p102">Die anderen **IMAPIProp** Methoden Berichten partiellen Erfolg unterschiedlich. Diese Methoden Bericht partiellen Erfolg von wird S_OK zur�ckgegeben, und platzieren Fehlerinformationen in eine [SPropProblemArray](spropproblemarray.md) -Struktur. Im Gegensatz zu der Arrays der Eigenschaft Wert in **GetProps**, das Daten unabh�ngig davon, ob die Methode erfolgreich war oder nicht enth�lt, ist das Array-Eigenschaft Problem in diesen Methoden nur, wenn Fehler aufgetreten sind, und nur, wenn der Aufrufer Zinsen kennenzulernen Fehler registriert hat vorhanden. Anrufer m�ssen einen g�ltiger **SPropProblemArray** Zeiger f�r Fehlerinformationen registriert angeben.</span><span class="sxs-lookup"><span data-stu-id="1eab5-p102">The other **IMAPIProp** methods report partial success differently. These methods report partial success by returning S_OK and placing error information in an [SPropProblemArray](spropproblemarray.md) structure. Unlike the property value array in **GetProps** that contains data regardless of whether the method succeeded or failed, the property problem array in these methods exists only if there are errors and only if the caller has registered interest in learning about the errors. Callers must specify a valid **SPropProblemArray** pointer to register for error information.</span></span> 
  
<span data-ttu-id="1eab5-p103">Wenn ein Fehlerwert von **SetProps**, **DeleteProps**, **CopyTo**oder **CopyProps**zur�ckgegeben wird, bedeutet dies Fehler anstelle von partiellen Erfolg. Das Array-Eigenschaft Problem ist gegebenenfalls ung�ltig. Clients sollte nicht versuchen, Zugriff auf Daten in der Struktur gehalten noch sollten sie versuchen, die Struktur selbst frei. Die entsprechende Antwort wird [IMAPIProp::GetLastError](imapiprop-getlasterror.md)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1eab5-p103">When an error value is returned from **SetProps**, **DeleteProps**, **CopyTo**, or **CopyProps**, this indicates failure instead of partial success. The property problem array, if available, is not valid. Clients should not try to access data held in the structure nor should they try to free the structure itself. The appropriate response is to call [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span> 
  
<span data-ttu-id="1eab5-p104">**GetLastError** ist vergleichbar mit der Funktion mit demselben Namen im Windows SDK bereitgestellt. Beide enthalten detailliertere Informationen zu einem Fehler als mit dem R�ckgabewert verf�gbar ist. Beide Zur�ckgeben von Informationen zu den vorherigen aufgetretenen Fehler. Der Unterschied besteht darin, dass die **GetLastError** Win32-Funktion einen Fehler vom aufrufenden meldet und die **IMAPIProp::GetLastError** -Methode ein Fehler generiert, die durch das aktuelle Objekt meldet. D. h., wenn ein Client **DeleteProps** f�r eine Nachricht und MAPI_E_NO_ACCESS aufruft wird um anzugeben, dass die Nachricht ist schreibgesch�tzt, **GetLastError** gibt Daten von der Nachricht zur�ckgegeben.</span><span class="sxs-lookup"><span data-stu-id="1eab5-p104">**GetLastError** is similar to the function of the same name provided in the Windows SDK. Both provide more detailed information about an error than is available with the return value. They both return information about the previous error that has occurred. The difference is that the Win32 **GetLastError** function reports on an error generated by the calling thread and the **IMAPIProp::GetLastError** method reports on an error generated by the current object. That is, if a client calls **DeleteProps** on a message and MAPI_E_NO_ACCESS is returned to indicate that the message is read-only, **GetLastError** returns data provided by the message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1eab5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1eab5-128">See also</span></span>

- [<span data-ttu-id="1eab5-129">�bersicht �ber die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1eab5-129">MAPI Property Overview</span></span>](mapi-property-overview.md)

