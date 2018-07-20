---
title: Zurückstellen MAPI-Fehler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93ae6d54-41cd-433c-8124-eb07d71baa57
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e2b091fa21dae4a1a8da23954d5f998010483da1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791507"
---
# <a name="deferring-mapi-errors"></a><span data-ttu-id="f7db2-103">Zurückstellen MAPI-Fehler</span><span class="sxs-lookup"><span data-stu-id="f7db2-103">Deferring MAPI Errors</span></span>

  
  
<span data-ttu-id="f7db2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7db2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7db2-p101">Einige Schnittstellenmethoden akzeptieren Sie die Kennzeichen MAPI_DEFERRED_ERRORS als Eingabeparameter. Wenn dieses Flag festgelegt ist, muss die Methode nicht sofort mit einem Wert zurückgegeben; Sie können den Anrufer das Ergebnis des Anrufs zu einem späteren Zeitpunkt wissen lassen.</span><span class="sxs-lookup"><span data-stu-id="f7db2-p101">Some interface methods accept the MAPI_DEFERRED_ERRORS flag as an input parameter. When this flag is set, the method does not have to return immediately with a value; it can let the caller know the result of the call at some later time.</span></span>
  
<span data-ttu-id="f7db2-p102">Zurückstellen Fehler hilft-Dienstanbieter in ihrer Implementierung der komplexe Methoden t�tigen schneller verarbeitet. Statt viele Anforderungen zu behandeln und Zurückgeben eines Werts für die einzelnen, kann Fehler verzögern der Anrufe für den Dienstanbieter geb�ndelt werden. Viele Anforderungen gleichzeitig verarbeitet senkt die Netzwerkdatenverkehr, wodurch die Leistung verbessert. Zurückstellen Fehler ist besonders hilfreich in Aufrufe l�schen oder Kopie-Eigenschaften, mit die Vorgänge sehr zeitaufwendig sein können.</span><span class="sxs-lookup"><span data-stu-id="f7db2-p102">Deferring errors helps service providers in their implementation of complex methods, making processing faster. Rather than handling many requests and returning a value for each, deferring errors allows the calls to be bundled within the service provider. Processing many requests at once cuts down on network traffic, thereby improving performance. Deferring errors is especially useful in calls to delete or copy properties, which can be very time-consuming operations.</span></span> 
  
<span data-ttu-id="f7db2-p103">Wenn ein Client einen Anruf ernannt werden, ohne das MAPI_DEFERRED_ERRORS-Flag festlegen, die verzögert nur behandelt werden kann, können Dienstanbieter entweder die Fehler ungefähre verzögern oder MAPI_E_TOO_COMPLEX zurückzugeben. Die meisten Clients sollte als Strategie vorzuziehen, dass Sie den Anruf defekt Fehler verzögern.</span><span class="sxs-lookup"><span data-stu-id="f7db2-p103">When a client makes a call without setting the MAPI_DEFERRED_ERRORS flag that can only be handled in a deferred manner, service providers can either defer the errors regardless or return MAPI_E_TOO_COMPLEX. Most clients should defer errors as a preferable strategy to failing the call.</span></span> 
  
<span data-ttu-id="f7db2-p104">Die Einstellung der MAPI_DEFERRED_ERRORS �ndert Flag Implementierung des Clients Fehlerbehandlung darin, dass die zurückgegebene Informationen können Sie jederzeit und nicht zu einem geplanten Zeitpunkt übermittelt werden kann. Es ist möglich, dass ein Fehler zurückgegeben werden soll, wenn es zu spät ist nichts davon oder nachdem Daten über die ursprüngliche Anforderung nicht mehr verfügbar ist. Beispielsweise wenn ein Client **IMsgStore::OpenEntry** um einen gelöschten Ordner mit MAPI_DEFERRED_ERRORS �ffnen aufruft, wird der Client nicht des Problems wissen, bis eine **IMAPIProp::GetProps** aufgerufen wird, um eine der Eigenschaften des Ordners abzurufen. **GetProps** gibt MAPI_E_NOT_FOUND zurück.</span><span class="sxs-lookup"><span data-stu-id="f7db2-p104">Setting the MAPI_DEFERRED_ERRORS flag changes a client's error handling implementation in that the returned information can be delivered at any time rather than at a planned time. It is possible for an error to be returned when it is too late to do anything about it or after data about the original request is no longer available. For example, if a client calls **IMsgStore::OpenEntry** to open a deleted folder with MAPI_DEFERRED_ERRORS set, the client will not know of the problem until an **IMAPIProp::GetProps** call is made to retrieve one of the folder's properties. **GetProps** will then return MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7db2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7db2-117">See also</span></span>



[<span data-ttu-id="f7db2-118">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f7db2-118">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="f7db2-119">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f7db2-119">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)

