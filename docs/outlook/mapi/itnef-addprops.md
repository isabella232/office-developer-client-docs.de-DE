---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fb9591794ae6606ef06b0fc756380fcd0ffab3fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610405"
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
  
> [in] Eine Bitmaske mit Flags, die steuert, wie Eigenschaften in die Kapselung eingeschlossen oder von dieser ausgeschlossen werden. Die folgenden Flags können festgelegt werden:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Codiert nur die Eigenschaften im  _lpPropList-Parameter,_ die Teil von Anlagen in der Nachricht sind. 
    
TNEF_PROP_CONTAINED 
  
> Codiert nur Eigenschaften aus der durch den  _ulElemID-Parameter_ angegebenen Anlage. Wenn der  _lpvData-Parameter_ nicht NULL ist, werden die Daten, auf die verwiesen wird, in die Kapselung der Anlage in der Datei geschrieben, die durch die **eigenschaft PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) angegeben wird.
    
TNEF_PROP_CONTAINED_TNEF 
  
> Codiert nur Eigenschaften aus der Nachricht oder Anlage, die durch den  _ulElemID-Parameter_ angegeben wird. Wenn dieses Flag festgelegt ist, muss der Wert in  _lpvData_ ein [IStream-Zeiger](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) sein. 
    
TNEF_PROP_EXCLUDE 
  
> Codiert alle Eigenschaften, die nicht im  _lpPropList-Parameter_ angegeben sind. 
    
TNEF_PROP_INCLUDE 
  
> Codiert alle in  _lpPropList_ angegebenen Eigenschaften. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Codiert nur die in  _lpPropList_ angegebenen Eigenschaften, die Teil der Nachricht selbst sind. 
    
 _ulElemID_
  
> [in] Die eigenschaft **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) einer Anlage, die eine Zahl enthält, die die Anlage in der übergeordneten Nachricht eindeutig identifiziert. Der  _ulElemID-Parameter_ wird verwendet, wenn eine spezielle Behandlung für eine Anlage angefordert wird. Der  _ulElemID-Parameter_ sollte 0 sein, es sei denn, das TNEF_PROP_CONTAINED- oder TNEF_PROP_CONTAINED_TNEF-Flag ist im  _ulFlags-Parameter_ festgelegt. 
    
 _lpvData_
  
> [in] Ein Zeiger auf Anlagendaten, die verwendet werden, um die Daten der in  _ulElemID_ angegebenen Anlage zu ersetzen. Der  _lpvData-Parameter_ sollte NULL sein, es sei denn, TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF in  _ulFlags_ festgelegt ist.
    
 _lpPropList_
  
> [in] Ein Zeiger auf die Liste der Eigenschaften, die in die Kapselung eingeschlossen oder von dieser ausgeschlossen werden sollen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::AddProps-Methode** auf, um Eigenschaften aufzuführen, die in die Transport-Neutral Kapselungsformatverarbeitung (Encapsulation Format, TNEF) einer Nachricht oder Anlage einbezogen oder ausgeschlossen werden sollen. Durch die Verwendung aufeinander folgender Aufrufe kann der Anbieter oder das Gateway eine Liste der Eigenschaften angeben, die hinzugefügt und codiert oder von der Codierung ausgeschlossen werden sollen. Anbieter und Gateways können **AddProps** auch verwenden, um Informationen zu speziellen Anlagen bereitzustellen, die behandelt werden sollten. 
  
 **AddProps** wird nur für TNEF-Objekte unterstützt, die mit dem TNEF_ENCODE Flag für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion](opentnefstreamex.md) geöffnet werden. 
  
Beachten Sie, dass für **AddProps** keine tatsächliche TNEF-Codierung erfolgt, bis die [ITnef::Finish-Methode](itnef-finish.md) aufgerufen wird. Diese Funktionalität bedeutet, dass an **AddProps** übergebene Zeiger bis nach dem Aufruf von **"Fertig stellen"** gültig bleiben müssen. An diesem Punkt können alle Objekte und Daten, die mit **AddProps-Aufrufen** übergeben werden, freigegeben oder freigegeben werden. 
  
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

