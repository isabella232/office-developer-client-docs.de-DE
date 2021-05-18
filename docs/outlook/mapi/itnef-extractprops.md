---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407501"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Extrahiert die Eigenschaften aus einer TNEF-Kapselung. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie Eigenschaften decodiert werden. Die folgenden Kennzeichen können festgelegt werden:
    
TNEF_PROP_EXCLUDE 
  
> Decodiert alle Eigenschaften, die nicht im  _lpPropList-Parameter angegeben_ sind. 
    
TNEF_PROP_INCLUDE 
  
> Decodiert alle in _lpPropList angegebenen Eigenschaften._
    
 _lpPropList_
  
> [in] Ein Zeiger auf die Liste der Eigenschaften, die in den Decodierungsvorgang aufgenommen oder aus dem Decodierungsvorgang ausgeschlossen werden.
    
 _lpProblems_
  
> [out] Ein Zeiger auf einen Zeiger auf eine zurückgegebene [STnefProblemArray-Struktur.](stnefproblemarray.md) Die **STnefProblemArray-Struktur** gibt an, welche Eigenschaften, falls welche, nicht ordnungsgemäß codiert wurden. Wenn NULL im  _lpProblems-Parameter_ übergeben wird, wird kein Eigenschaftsproblemarray zurückgegeben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
MAPI_E_CORRUPT_DATA 
  
> Daten, die in einen Datenstrom decodiert werden, sind beschädigt.
    
## <a name="remarks"></a>Hinweise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::ExtractProps-Methode** auf, um Eigenschaften aus der Kapselung einer Nachricht oder einer Anlage zu extrahieren (d. h. zu decodieren), die an die [OpenTnefStream-Funktion](opentnefstream.md) übergeben wurde. Der aufrufende Anbieter oder das Gateway kann eine Liste der zu decodierenden Eigenschaften angeben. Anbieter und Gateways können **extractProps** auch verwenden, um Informationen zu einer speziellen Behandlung von Anlagen zur Verfügung zu stellen. 
  
 **ExtractProps** füllt die ursprüngliche Nachricht, die an **OpenTnefStream** übergeben wurde, mit den decodierten Eigenschaften auf. Nachfolgende **ExtractProps-Aufrufe** gehen zurück zur Nachricht, und extrahieren Sie die neue Liste der Eigenschaften. 
  
Im Gegensatz zur [ITnef::AddProps-Methode,](itnef-addprops.md) die angeforderte Aktionen in die Warteschlange einreiht, bis die **ITnef::Finish-Methode** aufgerufen wird, decodiert die **ExtractProps-Methode** die gekapselten Eigenschaften sofort, wenn sie aufgerufen wird. Aus diesem Grund sollte die Zielnachricht für die Kapselungsdecodierung relativ leer sein. Vorhandene Eigenschaften in der Zielnachricht werden durch gekapselte Eigenschaften überschrieben. 
  
 **ExtractProps wird** nur für Objekte unterstützt, die mit dem TNEF_DECODE für die **OpenTnefStream-** oder [OpenTnefStreamEx-Funktion geöffnet](opentnefstreamex.md) werden. 
  
Die TNEF-Implementierung meldet TNEF-Streamcodierungsprobleme, ohne den **ExtractProps-Prozess zu** beenden. Die in _lpProblems_ zurückgegebene [STnefProblemArray-Struktur](stnefproblemarray.md) gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften (falls welche) nicht verarbeitet werden konnten. Der im **scode-Element** der in **STnefProblemArray enthaltene STnefProblemProblem-Struktur** zurückgegebene Wert gibt das spezifische Problem an.  Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **ExtractProps** keinen Problembericht zurück gibt, erfolgreich verarbeitet wurden. 
  
> [!NOTE]
> Wenn eine Eigenschaft im MAPI-Kapselungsblock nicht verarbeitet werden kann und der Datenstrom während der Decodierung eines TNEF-Datenstroms unzuverlässig bleibt, wird die Decodierung des Kapselungsblocks beendet, und es wird ein Problem gemeldet. Das Problemarray für diese Art von Problem enthält 0L für das **ulPropTag-Element** oder für das `attMAPIProps` `attAttachment` **ulAttribute-Element** und MAPI_E_UNABLE_TO_COMPLETE für das **scode-Element.** Beachten Sie, dass die Decodierung des Datenstroms nicht angehalten wird, sondern nur die Decodierung des MAPI-Kapselungsblocks. Die Datenstromdecodierung wird mit dem nächsten Attributblock fortgesetzt. 
  
Wenn ein Anbieter oder Gateway nicht mit Problemarrays funktioniert, kann er NULL in  _lppProblems übergeben._ In diesem Fall wird kein Problemarray zurückgegeben. 
  
Der in  _lpProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf eine S_OK. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die in der **STnefProblemArray-Struktur** zurückgegebenen Werte überprüfen. Wenn beim Anruf ein Fehler auftritt, wird die **STnefProblemArray-Struktur** nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder frei geben. Wenn beim Aufruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Arbeitsspeicher für die **STnefProblemArray-Struktur** durch Aufrufen der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) los. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

