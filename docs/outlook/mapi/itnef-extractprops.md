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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 26949f10e22c4d2ea49594ee3365ae7d3bb3662d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792870"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**Betrifft**: Outlook 
  
Extrahiert die Eigenschaften von TNEF-Kapselung. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie Eigenschaften decodiert werden. Die folgenden Kennzeichen können festgelegt werden:
    
TNEF_PROP_EXCLUDE 
  
> Decodiert alle Eigenschaften in der _LpPropList_ -Parameter nicht angegeben. 
    
TNEF_PROP_INCLUDE 
  
> Decodiert alle Eigenschaften in _LpPropList_angegeben.
    
 _lpPropList_
  
> [in] Ein Zeiger auf die Liste der Eigenschaften ein-oder Ausschließen von der Decodierung Operation.
    
 _lpProblems_
  
> [out] Ein Zeiger auf einen Zeiger auf eine zurückgegebenen [STnefProblemArray](stnefproblemarray.md) -Struktur. Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden. Wenn NULL in der _LpProblems_ -Parameter übergeben wird, wird kein Problem Array-Eigenschaft zurückgegeben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
MAPI_E_CORRUPT_DATA 
  
> In einem Stream decodierte Daten ist beschädigt.
    
## <a name="remarks"></a>Bemerkungen

Transport-Provider, Anbieter Nachricht und Gateways rufen die **ITnef::ExtractProps** -Methode zum Extrahieren von (das Decodieren ist,) Eigenschaften aus der Kapselung einer Nachricht oder einer Anlage, die an die Funktion [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) übergeben wurde. Die aufrufende Anbieter oder Gateway kann eine Liste der Eigenschaften zum Decodieren angeben. Anbieter und Gateways können **ExtractProps** auch Informationen zur keine besondere Behandlung für Anlagen aktualisiert. 
  
 **ExtractProps** füllt die ursprüngliche Nachricht in **OpenTNEFStream nicht ausgeführt werden** mit den Eigenschaften decodierten übergeben. Nachfolgende **ExtractProps** Aufrufe zurück an die Nachricht, und extrahieren Sie die neue Liste der Eigenschaften. 
  
Im Gegensatz zu der [ITnef::AddProps](itnef-addprops.md) -Methode, die Warteschlangen Aktionen angefordert, bis die **ITnef::Finish** -Methode aufgerufen wird, decodiert die **ExtractProps** -Methode die gekapselten Eigenschaften sofort, wenn sie aufgerufen wird. Aus diesem Grund sollten die Zielnachricht für die Decodierung Encapsulation relativ leer sein. Vorhandene Eigenschaften in der Zielnachricht werden von gekapselte Eigenschaften überschrieben. 
  
 **ExtractProps** wird nur für Objekte unterstützt, die mit dem TNEF_DECODE-Flag für die Funktion **OpenTNEFStream nicht ausgeführt werden** oder [OpenTnefStreamEx](opentnefstreamex.md) geöffnet werden. 
  
Die TNEF-Implementierung Berichte TNEF-Stream Probleme ohne Anhalten des Prozesses **ExtractProps** -Codierung. Die [STnefProblemArray](stnefproblemarray.md) -Struktur, die in _LpProblems_ zurückgegeben gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnte. Der im **Scode** -Member, eine der in **STnefProblemArray** enthaltenen **STnefProblem** Strukturen zurückgegebene Wert gibt an, das Problem. Der Anbieter oder Gateway kann auf der Annahme arbeiten, dass alle Eigenschaften oder Attribute, die für die **ExtractProps** kein Problemberichts zurückgibt erfolgreich verarbeitet wurden. 
  
> [!NOTE]
> Wenn eine Eigenschaft im MAPI-Kapselung Block kann nicht verarbeitet werden und den Stream während der Decodierung eines Streams TNEF unzuverlässig lässt, Decodieren des Blocks Encapsulation wurde beendet und ein Problem gemeldet wird. Das Problem Array für diese Art von Problem enthält 0L für den **UlPropTag** -Member, `attMAPIProps` oder `attAttachment` für **UlAttribute** Member und MAPI_E_UNABLE_TO_COMPLETE für den **Scode** -Member. Beachten Sie, dass die Decodierung des Datenstroms nicht angehalten, nur die Decodierung des MAPI-Kapselung Blocks. Der Datenstrom Decodierung wird mit dem nächsten Attributblock fortgesetzt. 
  
Wenn Sie einen Anbieter oder ein Gateway mit Problem Arrays nicht funktionsfähig ist, können sie NULL _LppProblems_übergeben; In diesem Fall wird kein Problem Array zurückgegeben. 
  
Der in _LpProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf gibt S_OK zurück. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder ein Gateway in der Struktur **STnefProblemArray** zurückgegebenen Werte überprüfen. Bei einem beim Aufruf Fehler die **STnefProblemArray** -Struktur ist nicht ausgefüllt und die aufrufende Anbieter oder das Gateway nicht verwenden oder die Struktur frei. Wenn dem Gespräch tritt kein Fehler auf, muss die aufrufende Anbieter oder Gateway des Speichers für die Struktur **STnefProblemArray** durch Aufrufen der Funktion [MAPIFreeBuffer](mapifreebuffer.md) freigeben. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

