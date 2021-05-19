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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416440"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verarbeitet einzelne Komponenten aus einer Nachricht einzeln in einen Transport-Neutral Encapsulation Format (TNEF).
  
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
  
> [in] Eine Bitmaske mit Flags, die steuert, welche Komponente fertig gestellt wird. Das eine oder andere der folgenden Kennzeichen muss festgelegt werden:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Die Verarbeitung für ein Anlagenobjekt wird abgeschlossen. Der  _ulComponentID-Parameter_ enthält **die PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft der Anlage. 
    
TNEF_COMPONENT_MESSAGE 
  
> Die Verarbeitung wird für ein Nachrichtenobjekt abgeschlossen. 
    
 _ulComponentID_
  
> [in] 0, um die Verarbeitung einer Nachricht oder die PR_ATTACH_NUM **einer** zu verarbeitenden Anlage anzugeben. Wenn das TNEF_COMPONENT_MESSAGE im  _ulFlags-Parameter_ festgelegt ist,  _muss ulComponentID_ 0 sein. 
    
 _lpCustomPropList_
  
> [in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die Eigenschaftstags enthält, die die im  _lpCustomProps-Parameter_ übergebenen Eigenschaften identifizieren. Es muss eine 1:1-Entsprechung zwischen jedem Eigenschaftswert in  _lpCustomProps_ und einem Eigenschaftstag im  _lpCustomPropList-Parameter_ liegen. 
    
 _lpCustomProps_
  
> [in] Ein Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die Eigenschaftswerte für die zu codierenden Eigenschaften enthält. 
    
 _lpPropList_
  
> [in] Ein Zeiger auf eine **SPropTagArray-Struktur,** die Eigenschaftstags für die zu codenden Eigenschaften enthält. 
    
 _lppProblems_
  
> [out] Ein Zeiger auf einen Zeiger auf eine zurückgegebene [STnefProblemArray-Struktur.](stnefproblemarray.md) Die **STnefProblemArray-Struktur** gibt an, welche Eigenschaften, falls welche, nicht ordnungsgemäß codiert wurden. Wenn NULL im  _lppProblems-Parameter_ übergeben wird, wird kein Array mit Eigenschaftsproblemen zurückgegeben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::FinishComponent-Methode** auf, um die TNEF-Verarbeitung für eine Komponente, entweder eine Nachricht oder eine Anlage, durchzuführen, wie durch das im  _ulFlags-Parameter_ festgelegte Flag angegeben wird. 
  
Damit die Komponentenverarbeitung aktiviert werden kann, übergeben der aufrufende Anbieter oder das Gateway das TNEF_COMPONENT_ENCODING-Flag in  _ulFlags_ für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion,](opentnefstreamex.md) die das Objekt geöffnet hat, um die Codierung zu empfangen. 
  
Bei der Übergabe von Werten in den  _Parametern lpCustomPropList_ und  _lpCustomProps_ wird eine Komponentencodierung durchgeführt, die der von der [ITnef::SetProps-Methode](itnef-setprops.md) durchgeführten Codierung entspricht. Das Übergeben eines Werts im  _lpPropList-Parameter_ führt eine Komponentencodierung durch, die der von der [ITnef::AddProps-Methode](itnef-addprops.md) mit dem in  _ulFlags_ festgelegten TNEF_PROP_INCLUDE entspricht. Wenn Sie diese Werte übergeben, können Sie Codierungen mit einem einzelnen Aufruf statt mit mehreren Aufrufen ausführen.
  
Die TNEF-Implementierung meldet TNEF-Streamcodierungsprobleme, ohne den **FinishComponent-Prozess zu** beenden. Die in _lppProblems_ zurückgegebene **STnefProblemArray-Struktur** gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften (falls welche) nicht verarbeitet werden konnten. Der im **scode-Element** der in **STnefProblemArray enthaltene STnefProblemProblem-Struktur** zurückgegebene Wert gibt das spezifische Problem an.  Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **FinishComponent** keinen Problembericht zurück gibt, erfolgreich verarbeitet wurden. 
  
Wenn ein Anbieter oder Gateway nicht mit Problemarrays funktioniert, kann er NULL in  _lppProblems übergeben._ In diesem Fall wird kein Problemarray zurückgegeben.
  
Der in  _lppProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf eine S_OK. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die in der [STnefProblemArray-Struktur](stnefproblemarray.md) zurückgegebenen Werte überprüfen. Wenn beim Anruf ein Fehler auftritt, wird die **STnefProblemArray-Struktur** nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder frei geben. Wenn beim Anruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Arbeitsspeicher für **das STnefProblemArray** durch Aufrufen der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) frei geben. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

