---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435677"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beendet die Verarbeitung aller TNEF-Vorgänge (Transport Neutral Encapsulation Format), die in der Warteschlange gespeichert sind. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpKey_
  
> Out Ein Zeiger auf die **PR_ATTACH_NUM** ([pidtagattachnumber (](pidtagattachnumber-canonical-property.md))-Schlüsseleigenschaft einer Anlage. Das TNEF-Kapselungs Objekt verwendet diesen Schlüssel, um eine Anlage mit dem Attachment-Platzierungs-Tag in einer Nachricht abzugleichen. Dieser Schlüssel sollte für jede Anlage eindeutig sein.
    
 _lpProblem_
  
> Out Ein Zeiger auf einen Zeiger auf eine zurückgegebene [STnefProblemArray](stnefproblemarray.md) -Struktur. Die **STnefProblemArray** -Struktur gibt an, welche Eigenschaften, falls vorhanden, nicht ordnungsgemäß codiert wurden. Wenn NULL im _lpProblem_ -Parameter übergeben wird, wird kein Property-Problem-Array zurückgegeben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef:: Finish** -Methode auf, um die Codierung aller Eigenschaften auszuführen, für die die Codierung in Aufrufen der [ITnef::](itnef-addprops.md) AddProps-und [ITnef:](itnef-setprops.md) : SetProps-Methoden angefordert wurde. Wenn das TNEF-Objekt mit dem TNEF_ENCODE-Flag für die [OpenTnefStream](opentnefstream.md) -oder die [OpenTnefStreamEx](opentnefstreamex.md) -Funktion geöffnet wurde, codiert die **Finish** -Methode die angeforderten Eigenschaften in den an dieses Objekt übergebenen Kapselungs Datenstrom. Wenn das TNEF-Objekt mit dem TNEF_DECODE-Flag geöffnet wurde, dekodiert die **Finish** -Methode die Eigenschaften aus dem TNEF-Stream und schreibt Sie zurück in die Nachricht, zu der Sie gehören. 
  
Nach dem **Finish** -Aufruf zeigt der Zeiger auf den Encapsulation-Stream auf das Ende der TNEF-Daten. Wenn der Anbieter oder das Gateway die TNEF-Streamdaten nach dem **Beendigungs** Aufruf verwenden muss, muss er den Stream-Zeiger auf den Anfang der TNEF-Datenstrom zurücksetzen. 
  
Die TNEF-Implementierung meldet TNEF-Datenstrom Codierungsprobleme, ohne den **Abschluss** Prozess zu beenden. Die im Parameter _lpProblem_ zurückgeGebene [STnefProblemArray](stnefproblemarray.md) -Struktur gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften, falls vorhanden, nicht verarbeitet werden konnten. Der Wert, der im **SCODE** -Element einer der in **STnefProblemArray** enthaltenen **STnefProblem** -Strukturen zurückgegeben wird, gibt das spezifische Problem an. Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **Finish** keinen Problembericht zurückgibt, erfolgreich verarbeitet wurden. 
  
Wenn ein Anbieter oder Gateway nicht mit Problem Arrays funktioniert, kann er in _lpProblem_den Wert NULL überschreiten; in diesem Fall wird kein Problem Array zurückgegeben. 
  
Der in _lpProblem_ zurückgegebene Wert ist nur gültig, wenn der Aufruf S_OK zurückgibt. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die in der **STnefProblemArray** -Struktur zurückgegebenen Werte überprüfen. Wenn für den Anruf ein Fehler auftritt, wird die **STnefProblemArray** -Struktur nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder freigeben. Wenn beim Aufruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Speicher für das **STnefProblemArray** freigeben, indem er die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion aufruft. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Datei. cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI verwendet die **ITnef:: Finish** -Methode, um die Verarbeitung des neuen TNEF-Streams abzuschließen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Kanonische Pidtagattachnumber (-Eigenschaft](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

