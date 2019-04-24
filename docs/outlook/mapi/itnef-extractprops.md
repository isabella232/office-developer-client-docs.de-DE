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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348650"
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
  
> in Eine Bitmaske von Flags, die Steuern, wie Eigenschaften decodiert werden. Die folgenden Flags können festgelegt werden:
    
TNEF_PROP_EXCLUDE 
  
> Decodiert alle Eigenschaften, die nicht im _lpPropList_ -Parameter angegeben sind. 
    
TNEF_PROP_INCLUDE 
  
> Decodiert alle in _lpPropList_angegebenen Eigenschaften.
    
 _lpPropList_
  
> in Ein Zeiger auf die Liste der Eigenschaften, die in den Decodierungsvorgang eingeschlossen oder daraus ausgeschlossen werden sollen.
    
 _lpProblems_
  
> Out Ein Zeiger auf einen Zeiger auf eine zurückgegebene [STnefProblemArray](stnefproblemarray.md) -Struktur. Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden. Wenn NULL im _lpProblems_ -Parameter übergeben wird, wird kein Property-Problem-Array zurückgegeben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
MAPI_E_CORRUPT_DATA 
  
> Daten, die in einem Stream decodiert werden, sind beschädigt.
    
## <a name="remarks"></a>Bemerkungen

Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef:: ExtractProps** -Methode auf, um Eigenschaften aus der Kapselung einer Nachricht oder einer Anlage, die an die [OpenTnefStream](opentnefstream.md) -Funktion übergeben wurde, zu extrahieren. Der aufrufende Anbieter oder das Gateway kann eine Liste der zu decodierenden Eigenschaften angeben. Anbieter und Gateways können auch **ExtractProps** verwenden, um Informationen zur Sonderbehandlung für Anlagen bereitzustellen. 
  
 **ExtractProps** füllt die ursprüngliche Nachricht, die an **OpenTnefStream** übergeben wurde, mit den decodierten Eigenschaften. Nachfolgende **ExtractProps** -Aufrufe gehen zurück auf die Nachricht und extrahieren die neue Liste mit Eigenschaften. 
  
Im Gegensatz zur [ITnef::](itnef-addprops.md) AddProps-Methode, die die angeforderten Aktionen in die Warteschlange stellt, bis die **ITnef:: Finish** -Methode aufgerufen wird, dekodiert die **ExtractProps** -Methode die gekapselt Eigenschaften sofort, wenn Sie aufgerufen wird. Aus diesem Grund sollte die Zielnachricht für die Kapselungs Decodierung relativ leer sein. Vorhandene Eigenschaften in der Zielnachricht werden durch gekapselte Eigenschaften überschrieben. 
  
 **ExtractProps** wird nur für Objekte unterstützt, die mit dem TNEF_DECODE-Flag für die **OpenTnefStream** -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion geöffnet werden. 
  
Die TNEF-Implementierung meldet TNEF-Datenstrom Codierungsprobleme, ohne den **ExtractProps** -Prozess zu beenden. Die in _lpProblems_ zurückgeGebene [STnefProblemArray](stnefproblemarray.md) -Struktur gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnten. Der Wert, der im **SCODE** -Element einer der in **STnefProblemArray** enthaltenen **STnefProblem** -Strukturen zurückgegeben wird, gibt das spezifische Problem an. Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **ExtractProps** keinen Problembericht zurückgibt, erfolgreich verarbeitet wurden. 
  
> [!NOTE]
> Wenn eine Eigenschaft im MAPI-Kapselungs Block nicht verarbeitet werden kann und der Datenstrom während der Decodierung eines TNEF-Streams unzuverlässig bleibt, wird die Decodierung des Kapselungs Blocks beendet und ein Problem gemeldet. Das Problem Array für diesen Problemtyp enthält 0L für das **ulPropTag** `attMAPIProps` -Element `attAttachment` oder für das **ulAttribute** -Element und MAPI_E_UNABLE_TO_COMPLETE für das **SCODE** -Element. Beachten Sie, dass die Decodierung des Streams nicht angehalten wird, sondern nur die Decodierung des MAPI-Kapselungs Blocks. Die Datenstrom Decodierung wird mit dem nächsten Attributblock fortgesetzt. 
  
Wenn ein Anbieter oder Gateway nicht mit Problem Arrays funktioniert, kann er in _lppProblems_den Wert NULL überschreiten; in diesem Fall wird kein Problem Array zurückgegeben. 
  
Der in _lpProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf S_OK zurückgibt. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die in der **STnefProblemArray** -Struktur zurückgegebenen Werte überprüfen. Wenn für den Anruf ein Fehler auftritt, wird die **STnefProblemArray** -Struktur nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder freigeben. Wenn beim Aufruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Speicher für die **STnefProblemArray** -Struktur freigeben, indem er die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufruft. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

