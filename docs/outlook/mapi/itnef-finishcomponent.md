---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7008549111f1b914cf2025c8d61ebc07196706fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792858"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Betrifft**: Outlook 
  
Verarbeitet aus einer Nachricht an eine einzelne Komponenten zu einem Zeitpunkt in einem Stream Transport-Neutral Encapsulation Format (TNEF).
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, welche Komponente abgeschlossen sein wird. Mindestens eine der anderen der folgenden Werte muss festgelegt werden:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Für ein Attachment-Objekt wird die Verarbeitung abgeschlossen werden; der Parameter _UlComponentID_ enthält die **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage. 
    
TNEF_COMPONENT_MESSAGE 
  
> Wird die Verarbeitung für ein Meldungsobjekt abgeschlossen werden. 
    
 _ulComponentID_
  
> [in] 0 bis zur Verarbeitung für eine Nachricht oder die **PR_ATTACH_NUM** -Eigenschaft einer Anlage zu verarbeitenden anzugeben. Wenn das Flag TNEF_COMPONENT_MESSAGE im _UlFlags_ -Parameter festgelegt ist, muss _UlComponentID_ 0 sein. 
    
 _lpCustomPropList_
  
> [in] Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die Eigenschaftentags enthält, mit denen die Eigenschaften im _LpCustomProps_ -Parameter übergeben. Es muss eine 1: 1-Beziehung zwischen den einzelnen Eigenschaftswert in _LpCustomProps_ und ein Tag-Eigenschaft im _LpCustomPropList_ -Parameter. 
    
 _lpCustomProps_
  
> [in] Ein Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die Eigenschaftswerte für die Eigenschaften, die zu codierende enthält. 
    
 _lpPropList_
  
> [in] Ein Zeiger auf eine **SPropTagArray** -Struktur, die für die Eigenschaften, die zu codierende Eigenschaftentags enthält. 
    
 _lppProblems_
  
> [out] Ein Zeiger auf einen Zeiger auf eine zurückgegebenen [STnefProblemArray](stnefproblemarray.md) -Struktur. Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden. Wenn NULL in der _LppProblems_ -Parameter übergeben wird, wird kein Problem Array-Eigenschaft zurückgegeben. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Transport-Anbieter, Nachricht-Anbieter und Gateways Aufruf der **ITnef::FinishComponent** -Methode von TNEF für eine Komponente, die eine Nachricht oder eine Anlage Verarbeitung ausführen, wie das Flag festlegen in der _UlFlags_ -Parameter angegeben. 
  
Für die Verarbeitung der Komponente aktiviert werden soll, übergeben die aufrufende Anbieter oder Gateway Sie die Kennzeichen TNEF_COMPONENT_ENCODING _UlFlags_ für die [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion, die das Objekt, um die Codierung wird geöffnet. 
  
Übergeben von Werten in den _LpCustomPropList_ und _LpCustomProps_ führt Komponente Codierung entspricht, die die [ITnef::SetProps](itnef-setprops.md) -Methode ausgeführt. Ein Wert in der _LpPropList_ -Parameter übergeben, führt Komponente Codierung entspricht, die von der [ITnef::AddProps](itnef-addprops.md) -Methode mit dem TNEF_PROP_INCLUDE-Flag festlegen in _UlFlags_erfolgen. Übergeben diese Werte können Sie mit einem einzigen Aufruf anstatt mehrere Aufrufe Codierungen ausführen.
  
Die TNEF-Implementierung Berichte TNEF-Stream Probleme ohne Anhalten des Prozesses **FinishComponent** -Codierung. Die **STnefProblemArray** -Struktur, die in _LppProblems_ zurückgegeben gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnte. Der im **Scode** -Member, eine der in **STnefProblemArray** enthaltenen **STnefProblem** Strukturen zurückgegebene Wert gibt an, das Problem. Der Anbieter oder Gateway kann auf der Annahme arbeiten, dass alle Eigenschaften oder Attribute, die für die **FinishComponent** kein Problemberichts zurückgibt erfolgreich verarbeitet wurden. 
  
Wenn Sie einen Anbieter oder ein Gateway mit Problem Arrays nicht funktionsfähig ist, können sie NULL _LppProblems_übergeben; In diesem Fall wird kein Problem Array zurückgegeben.
  
Der in _LppProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf gibt S_OK zurück. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder ein Gateway in der Struktur [STnefProblemArray](stnefproblemarray.md) zurückgegebenen Werte überprüfen. Bei einem beim Aufruf Fehler die **STnefProblemArray** -Struktur ist nicht ausgefüllt, und die aufrufende Anbieter oder das Gateway nicht verwenden oder die Struktur frei. Wenn dem Gespräch tritt kein Fehler auf, muss die aufrufende Anbieter oder Gateway den Speicher freizugeben für die **STnefProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

