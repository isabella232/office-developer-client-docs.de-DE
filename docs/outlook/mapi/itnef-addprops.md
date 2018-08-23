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
ms.openlocfilehash: e9d6b2b738ec16000612f41023f0fd46ceabf56f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589518"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ermöglicht die aufrufende Dienstanbieter oder Gateway Eigenschaften, die Kapselung einer Nachricht oder eine Anlage hinzuzufügen. 
  
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
  
> [in] Eine Bitmaske aus Flags, die steuert, wie Eigenschaften eingeschlossen oder ausgeschlossen Kapselung. Die folgenden Kennzeichen können festgelegt werden:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Nur die Eigenschaften im _LpPropList_ -Parameter, die Teil von Anlagen in der Nachricht sind codiert. 
    
TNEF_PROP_CONTAINED 
  
> Nur Eigenschaften aus der Anlage, die durch den _UlElemID_ -Parameter angegebenen codiert. Wenn der Parameter _LpvData_ nicht NULL ist, werden die Daten, auf in die Anlage-Kapselung in der durch die **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))-Eigenschaft angegebenen Datei geschrieben.
    
TNEF_PROP_CONTAINED_TNEF 
  
> Nur Eigenschaften aus der Nachricht oder einer Anlage, die durch den _UlElemID_ -Parameter angegebenen codiert. Wenn dieses Flag festgelegt ist, muss der Wert in _LpvData_ ein [IStream](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istream) Zeiger sein. 
    
TNEF_PROP_EXCLUDE 
  
> Codiert alle Eigenschaften in der _LpPropList_ -Parameter nicht angegeben. 
    
TNEF_PROP_INCLUDE 
  
> Alle Eigenschaften in _LpPropList_codiert. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Nur die Eigenschaften im _LpPropList_ angegeben, die Teil einer Nachricht sind codiert. 
    
 _ulElemID_
  
> [in] Eine Anlage **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))-Eigenschaft, die eine Zahl, eindeutig enthält identifiziert die Anlage in der übergeordneten Nachricht. Der Parameter _UlElemID_ wird verwendet, wenn besondere Behandlung für eine Anlage angefordert wird. Der Parameter _UlElemID_ muss 0 sein, es sei denn, das Flag TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF im _UlFlags_ -Parameter festgelegt ist. 
    
 _lpvData_
  
> [in] Ein Zeiger auf Anlagedaten verwendet, um die Daten der Anlage in _UlElemID_angegebenen ersetzen. Der Parameter _LpvData_ sollte NULL sein, es sei denn, TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF in _UlFlags_festgelegt ist.
    
 _lpPropList_
  
> [in] Ein Zeiger auf die Liste der Eigenschaften ein-oder Ausschließen von Kapselung.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Transport-Provider, Anbieter Nachricht und Gateways rufen Sie die **ITnef::AddProps** -Methode, die Listeneigenschaften aufgenommen oder aus der Verarbeitung Transport-Neutral Encapsulation Format (TNEF) einer Nachricht oder eine Anlage ausgeschlossen werden. Mithilfe von aufeinander folgenden aufrufen, kann die Anbieter oder das Gateway angeben eine Liste der Eigenschaften, die Sie hinzufügen und codieren oder ausgeschlossen werden codiert. Anbieter und Gateways können **AddProps** auch zum Bereitstellen von Informationen über alle Anlagen besondere Behandlung gewährt werden soll. 
  
 **AddProps** wird nur für TNEF-Objekten unterstützt, die mit dem TNEF_ENCODE-Flag für die Funktion [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder [OpenTnefStreamEx](opentnefstreamex.md) geöffnet werden. 
  
Beachten Sie, dass keine tatsächliche TNEF-Codierung geschieht für **AddProps** , bis die [ITnef::Finish](itnef-finish.md) -Methode aufgerufen wird. Dies bedeutet, dass Zeiger in **AddProps** übergeben gültig bis bleiben müssen nach dem Anruf auf **Fertig stellen** . An dieser Stelle können alle Objekte und Daten mit **AddProps** Anrufe übergebene freigegeben oder freigegeben werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI (engl.) verwendet die **ITnef::AddProps** -Methode, um Eigenschaften aus einer Nachricht in einem Stream TNEF zu kopieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachTransportName (kanonische Eigenschaft)](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

