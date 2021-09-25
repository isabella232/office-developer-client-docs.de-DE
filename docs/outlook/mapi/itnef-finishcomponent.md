---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a516476efd8a26dbd4953a3c16121c93beb6264f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561341"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verarbeitet einzelne Komponenten aus einer Nachricht nacheinander in einem Transport-Neutral Encapsulation Format (TNEF)-Datenstrom.
  
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
  
> [in] Eine Bitmaske mit Flags, die steuert, welche Komponente abgeschlossen wird. Eines der folgenden Flags muss festgelegt werden:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Die Verarbeitung für ein Anlagenobjekt wird abgeschlossen. der  _ulComponentID-Parameter_ enthält die **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) -Eigenschaft der Anlage. 
    
TNEF_COMPONENT_MESSAGE 
  
> Die Verarbeitung für ein Nachrichtenobjekt wird abgeschlossen. 
    
 _ulComponentID_
  
> [in] 0, um die Verarbeitung für eine Nachricht oder die **PR_ATTACH_NUM** Eigenschaft einer Anlage anzugeben, die verarbeitet werden soll. Wenn das flag TNEF_COMPONENT_MESSAGE im  _ulFlags-Parameter_ festgelegt ist, muss  _ulComponentID_ 0 sein. 
    
 _lpCustomPropList_
  
> [in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die Eigenschaftstags enthält, die die im  _lpCustomProps-Parameter übergebenen_ Eigenschaften identifizieren. Es muss eine 1:1-Entsprechung zwischen jedem Eigenschaftswert in  _lpCustomProps_ und einem Eigenschaftstag im  _lpCustomPropList-Parameter_ vorhanden sein. 
    
 _lpCustomProps_
  
> [in] Ein Zeiger auf eine [SPropValue-Struktur,](spropvalue.md) die Eigenschaftswerte für die zu codierenden Eigenschaften enthält. 
    
 _lpPropList_
  
> [in] Ein Zeiger auf eine **SPropTagArray-Struktur,** die Eigenschaftstags für die zu codierenden Eigenschaften enthält. 
    
 _lppProblems_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [zurückgegebene STnefProblemArray-Struktur.](stnefproblemarray.md) Die **STnefProblemArray-Struktur** gibt an, welche Eigenschaften ggf. nicht ordnungsgemäß codiert wurden. Wenn NULL im  _Parameter lppProblems_ übergeben wird, wird kein Eigenschaftsproblemarray zurückgegeben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::FinishComponent-Methode** auf, um die TNEF-Verarbeitung für eine Komponente auszuführen, entweder eine Nachricht oder eine Anlage, wie durch das im  _ulFlags-Parameter_ festgelegte Flag angegeben. 
  
Damit die Komponentenverarbeitung aktiviert ist, übergibt der aufrufende Anbieter oder das Gateway das TNEF_COMPONENT_ENCODING Flag in  _ulFlags_ für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion,](opentnefstreamex.md) die das Objekt zum Empfangen der Codierung geöffnet hat. 
  
Durch Übergeben von Werten in den  _Parametern lpCustomPropList_ und  _lpCustomProps_ wird eine Komponentencodierung ausgeführt, die der von der [ITnef::SetProps-Methode](itnef-setprops.md) durchgeführten Codierung entspricht. Das Übergeben eines Werts im  _Parameter lpPropList_ führt eine Komponentencodierung durch, die der von der [ITnef::AddProps](itnef-addprops.md) -Methode mit dem in  _ulFlags_ festgelegten TNEF_PROP_INCLUDE Flag entspricht. Wenn Sie diese Werte übergeben, können Sie Codierungen mit einem einzigen Aufruf anstelle mehrerer Aufrufe ausführen.
  
Die TNEF-Implementierung meldet TNEF-Datenstromcodierungsprobleme, ohne den **FinishComponent-Prozess zu** beenden. Die in _lppProblems_ zurückgegebene **STnefProblemArray-Struktur** gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften ggf. nicht verarbeitet werden konnten. Der Wert, der im **Scode-Element** einer der in **STnefProblemArray enthaltenen STnefProblemArray-Strukturen** zurückgegeben wird, gibt das spezifische Problem an.  Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **FinishComponent** keinen Problembericht zurückgibt, erfolgreich verarbeitet wurden. 
  
Wenn ein Anbieter oder Gateway nicht mit Problemarrays funktioniert, kann er NULL in  _lppProblems_ übergeben; in diesem Fall wird kein Problemarray zurückgegeben.
  
Der in  _lppProblems zurückgegebene_ Wert ist nur gültig, wenn der Aufruf S_OK zurückgibt. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die werte überprüfen, die in der [STnefProblemArray-Struktur](stnefproblemarray.md) zurückgegeben werden. Wenn beim Anruf ein Fehler auftritt, wird die **STnefProblemArray-Struktur** nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder freigeben. Wenn beim Anruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Speicher für **STnefProblemArray** freigeben, indem er die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufruft. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

