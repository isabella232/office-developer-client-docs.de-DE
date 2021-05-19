---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348622"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht dem aufrufenden Dienstanbieter oder Gateway das Hinzufügen von Eigenschaften zur Kapselung einer Nachricht oder Anlage. 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske von Flags, die steuert, wie Eigenschaften in die Kapselung eingeschlossen oder von der Kapselung ausgeschlossen werden. Die folgenden Kennzeichen können festgelegt werden:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Codiert nur die Eigenschaften im  _lpPropList-Parameter,_ die Teil von Anlagen in der Nachricht sind. 
    
TNEF_PROP_CONTAINED 
  
> Codiert nur Eigenschaften aus der anlage, die durch den  _ulElemID-Parameter angegeben_ wird. Wenn der  _lpvData-Parameter_ nicht NULL ist, werden die daten, auf die verwiesen wird, in die Kapselung der Anlage in der Datei geschrieben, die durch die **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) -Eigenschaft angegeben wird.
    
TNEF_PROP_CONTAINED_TNEF 
  
> Codiert nur Eigenschaften aus der Nachricht oder Anlage, die durch den  _ulElemID-Parameter angegeben_ wird. Wenn dieses Flag festgelegt ist, muss der Wert in  _lpvData_ ein [IStream-Zeiger](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) sein. 
    
TNEF_PROP_EXCLUDE 
  
> Codiert alle Eigenschaften, die nicht im  _lpPropList-Parameter angegeben_ sind. 
    
TNEF_PROP_INCLUDE 
  
> Codiert alle in  _lpPropList_ angegebenen Eigenschaften. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Codiert nur die in  _lpPropList_ angegebenen Eigenschaften, die Teil der Nachricht selbst sind. 
    
 _ulElemID_
  
> [in] Die eigenschaft PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) einer Anlage, die eine Zahl enthält, die die Anlage in ihrer übergeordneten Nachricht eindeutig identifiziert. Der  _ulElemID-Parameter_ wird verwendet, wenn eine spezielle Behandlung für eine Anlage angefordert wird. Der  _ulElemID-Parameter_ sollte 0 sein, es sei denn, TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF im  _ulFlags-Parameter festgelegt_ ist. 
    
 _lpvData_
  
> [in] Ein Zeiger auf Anlagendaten, die zum Ersetzen der In _ulElemID angegebenen Anlagendaten verwendet werden._ Der _lpvData-Parameter_ sollte NULL sein, es sei denn, TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF in _ulFlags festgelegt ist._
    
 _lpPropList_
  
> [in] Ein Zeiger auf die Liste der Eigenschaften, die in die Kapselung aufgenommen oder von der Kapselung ausgeschlossen werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::AddProps-Methode** auf, um Eigenschaften auflisten, die in die Transport-Neutral Encapsulation Format (TNEF)-Verarbeitung einer Nachricht oder Anlage eingeschlossen oder von dieser ausgeschlossen werden sollen. Durch die Verwendung aufeinander folgenden Aufrufs kann der Anbieter oder das Gateway eine Liste der Eigenschaften angeben, die hinzugefügt und codiert oder von der Codierung ausgeschlossen werden. Anbieter und Gateways können auch **AddProps** verwenden, um Informationen zu speziellen Behandlungsanlagen zur Verfügung zu stellen. 
  
 **AddProps wird** nur für TNEF-Objekte unterstützt, die mit dem TNEF_ENCODE für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion geöffnet](opentnefstreamex.md) werden. 
  
Beachten Sie, dass keine tatsächliche TNEF-Codierung für **AddProps** erfolgt, bis die [ITnef::Finish-Methode](itnef-finish.md) aufgerufen wird. Diese Funktionalität bedeutet, dass Zeiger, die an **AddProps übergeben** werden, gültig bleiben müssen, bis der Aufruf von **Finish** erfolgt ist. An diesem Punkt können alle Objekte und Daten, die mit **AddProps-Aufrufen** übergeben werden, freigegeben oder freigegeben werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI verwendet die **ITnef::AddProps-Methode,** um Eigenschaften aus einer Nachricht in einen TNEF-Stream zu kopieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachTransportName (kanonische Eigenschaft)](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

