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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
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
  
> in Eine Bitmaske von Flags, die steuert, wie Eigenschaften in Kapselung eingeschlossen oder von dieser ausgeschlossen werden. Die folgenden Flags können festgelegt werden:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Codiert nur die Eigenschaften im _lpPropList_ -Parameter, die Teil von Anlagen in der Nachricht sind. 
    
TNEF_PROP_CONTAINED 
  
> Codiert nur Eigenschaften aus der Anlage, die durch den _ulElemID_ -Parameter angegeben wird. Wenn der _lpvData_ -Parameter nicht NULL ist, werden die Daten, auf die verwiesen wird, in die Kapselung der Anlage in der durch die **PR_ATTACH_TRANSPORT_NAME** ([pidtagattachtransportname (](pidtagattachtransportname-canonical-property.md))-Eigenschaft angegebenen Datei geschrieben.
    
TNEF_PROP_CONTAINED_TNEF 
  
> Codiert nur Eigenschaften aus der Nachricht oder Anlage, die durch den _ulElemID_ -Parameter angegeben wird. Wenn dieses Flag festgelegt ist, muss der Wert in _lpvData_ ein [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) -Zeiger sein. 
    
TNEF_PROP_EXCLUDE 
  
> Codiert alle Eigenschaften, die nicht im _lpPropList_ -Parameter angegeben sind. 
    
TNEF_PROP_INCLUDE 
  
> Codiert alle in _lpPropList_angegebenen Eigenschaften. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Codiert nur die in _lpPropList_ angegebenen Eigenschaften, die Teil der Nachricht selbst sind. 
    
 _ulElemID_
  
> in Die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Eigenschaft einer Anlage, die eine Zahl enthält, die die Anlage in der übergeordneten Nachricht eindeutig identifiziert. Der Parameter _ulElemID_ wird verwendet, wenn eine spezielle Behandlung für eine Anlage angefordert wird. Der _ulElemID_ -Parameter sollte 0 sein, es sei denn, das TNEF_PROP_CONTAINED-oder TNEF_PROP_CONTAINED_TNEF-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _lpvData_
  
> in Ein Zeiger auf Anlagendaten, die zum Ersetzen der Daten der in _ulElemID_angegebenen Anlage verwendet werden. Der _lpvData_ -Parameter sollte NULL sein, es sei denn, TNEF_PROP_CONTAINED oder TNEF_PROP_CONTAINED_TNEF ist in _ulFlags_festgelegt.
    
 _lpPropList_
  
> in Ein Zeiger auf die Liste der Eigenschaften, die in Kapselung eingeschlossen oder von dieser ausgeschlossen werden sollen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Transportanbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef::** AddProps-Methode auf, um Eigenschaften aufzulisten, die in die TNEF-Verarbeitung (Transport Neutral Encapsulation Format) einer Nachricht oder Anlage eingeschlossen werden sollen. Durch die Verwendung aufeinanderfolgender Aufrufe kann der Anbieter oder das Gateway eine Liste von Eigenschaften angeben, die hinzugefügt und codiert werden sollen. Anbieter und Gateways können auch addProps verwenden, um Informationen über sonderbehandlungs Anlagen bereitzustellen. **** 
  
 **** AddProps wird nur für TNEF-Objekte unterstützt, die mit dem TNEF_ENCODE-Flag für die [OpenTnefStream](opentnefstream.md) -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion geöffnet werden. 
  
Beachten Sie, dass keine tatsächliche TNEF- **** Codierung für AddProps erfolgt, bis die [ITnef:: Finish](itnef-finish.md) -Methode aufgerufen wird. Diese Funktionalität bedeutet, dass Zeiger, **** die an AddProps übergeben werden, gültig bleiben müssen, bis der Aufruf **beendet** wurde. An diesem Punkt können alle Objekte und Daten, die mit **** AddProps-aufrufen übergeben wurden, freigegeben oder befreit werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Datei. cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI verwendet die **ITnef::** AddProps-Methode, um Eigenschaften aus einer Nachricht in einen TNEF-Stream zu kopieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Kanonische Pidtagattachtransportname (-Eigenschaft](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

