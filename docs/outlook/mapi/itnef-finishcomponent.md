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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278886"
---
# <a name="itneffinishcomponent"></a>ITnef::FinishComponent

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verarbeitet einzelne Komponenten aus einer Nachricht nacheinander in einen TNEF-Stream (Transport Neutral Encapsulation Format).
  
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
  
> in Eine Bitmaske von Flags, die steuert, welche Komponente beendet wird. Eine der folgenden Flags muss festgelegt werden:
    
TNEF_COMPONENT_ATTACHMENT 
  
> Die Verarbeitung wird für ein Attachment-Objekt beendet; der Parameter _ulComponentID_ enthält die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft der Anlage. 
    
TNEF_COMPONENT_MESSAGE 
  
> Die Verarbeitung wird für ein Message-Objekt abgeschlossen. 
    
 _ulComponentID_
  
> [in] 0, um die Verarbeitung für eine Nachricht anzugeben, oder die **PR_ATTACH_NUM** -Eigenschaft einer Anlage, die verarbeitet werden soll. Wenn das TNEF_COMPONENT_MESSAGE-Flag im _ulFlags_ -Parameter festgelegt ist, muss _ulComponentID_ 0 sein. 
    
 _lpCustomPropList_
  
> in Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die Eigenschaftstags enthält, die die im _lpCustomProps_ -Parameter übergebenen Eigenschaften identifizieren. Es muss eine 1:1-Entsprechung zwischen jedem Eigenschaftswert in _lpCustomProps_ und einem Property-Tag im _LpCustomPropList_ -Parameter vorhanden sein. 
    
 _lpCustomProps_
  
> in Ein Zeiger auf eine [SPropValue](spropvalue.md) -Struktur, die Eigenschaftswerte für die zu codierenden Eigenschaften enthält. 
    
 _lpPropList_
  
> in Ein Zeiger auf eine **SPropTagArray** -Struktur, die Eigenschaftentags für die zu codierenden Eigenschaften enthält. 
    
 _lppProblems_
  
> Out Ein Zeiger auf einen Zeiger auf eine zurückgegebene [STnefProblemArray](stnefproblemarray.md) -Struktur. Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden. Wenn NULL im _lppProblems_ -Parameter übergeben wird, wird kein Property-Problem-Array zurückgegeben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef:: FinishComponent** -Methode auf, um die TNEF-Verarbeitung für eine Komponente, entweder eine Nachricht oder eine Anlage auszuführen, wie durch das im _ulFlags_ -Parameter festgelegte Flag angegeben. 
  
Zur Aktivierung der Komponentenverarbeitung übergibt der aufrufende Anbieter oder das Gateway das TNEF_COMPONENT_ENCODING-Flag in _ulFlags_ für die [OpenTnefStream](opentnefstream.md) -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion, die das Objekt zum Empfangen der Codierung geöffnet hat. 
  
Das übergeben von Werten in den Parametern _lpCustomPropList_ und _lpCustomProps_ führt eine Komponenten Codierung aus, die der [ITnef::](itnef-setprops.md) SetProps-Methode entspricht. Durch das Übergeben eines Werts im _lpPropList_ -Parameter wird die Komponenten Codierung ausgeführt, die der [ITnef::](itnef-addprops.md) AddProps-Methode mit dem in _ULFLAGS_festgelegten TNEF_PROP_INCLUDE-Flag entspricht. Durch das Übergeben dieser Werte können Sie Codierungen mit einem einzelnen Aufruf anstelle mehrerer Aufrufe durchführen.
  
Die TNEF-Implementierung meldet TNEF-Datenstrom Codierungsprobleme, ohne den **FinishComponent** -Prozess zu beenden. Die in _lppProblems_ zurückgeGebene **STnefProblemArray** -Struktur gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnten. Der Wert, der im **SCODE** -Element einer der in **STnefProblemArray** enthaltenen **STnefProblem** -Strukturen zurückgegeben wird, gibt das spezifische Problem an. Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **FinishComponent** keinen Problembericht zurückgibt, erfolgreich verarbeitet wurden. 
  
Wenn ein Anbieter oder Gateway nicht mit Problem Arrays funktioniert, kann er in _lppProblems_den Wert NULL überschreiten; in diesem Fall wird kein Problem Array zurückgegeben.
  
Der in _lppProblems_ zurückgegebene Wert ist nur gültig, wenn der Aufruf S_OK zurückgibt. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die in der [STnefProblemArray](stnefproblemarray.md) -Struktur zurückgegebenen Werte überprüfen. Wenn für den Anruf ein Fehler auftritt, wird die **STnefProblemArray** -Struktur nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder freigeben. Wenn beim Aufruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Speicher für das **STnefProblemArray** freigeben, indem er die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufruft. 
  
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[SPropTagArray](sproptagarray.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

