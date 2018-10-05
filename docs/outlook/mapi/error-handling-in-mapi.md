---
title: Fehlerbehandlung in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401692"
---
# <a name="error-handling-in-mapi"></a>Fehlerbehandlung in MAPI

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erfolg, Warnung und Fehler-Werte werden unter Verwendung einer 32-Bit-Version bekannte dementsprechend Handle oder HRESULT zurückgegeben. Ein HRESULT ist nicht wirklich ein Handle auf einen anderen Wert. Es wird lediglich eine 32-Bit-Wert mit mehrere Felder in den Wert codiert. Ein NULL-Ergebnis zeigt Erfolg und ein ungleich NULL Ergebnis Fehler.
  
MAPI auf 32-Bit-Plattformen funktioniert nur mit HRESULT-Werte.
  
Die folgende Abbildung zeigt das HRESULT-Format für 32-Bit-Plattformen.
  
**HRESULT-Format**
  
![HRESULT-format] (media/amapi_49.gif "HRESULT-format")
  
Das hohe Bit in der HRESULT gibt an, ob der Rückgabewert Erfolg oder Fehler darstellt. Wenn der Wert Erfolg gibt 0 (null) festgelegt, an. Wenn auf 1 festgelegt, es einen Fehler angibt.
  
Die R, C, N und R Bits sind in der HRESULT reserviert.
  
Das Feld Facility in beiden Versionen gibt den Bereich der Verantwortung für den Fehler. Es gibt verschiedene Funktionen, aber die Mehrheit der MAPI-Fehler verwenden FACILITY_ITF Benutzeroberflächenfehler darstellen. Werden die am häufigsten verwendeten Funktionen, die derzeit verwendet werden: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC und FACILITY_STORAGE. Wenn neue Funktionen erforderlich sind, weist Microsoft sie, da sie eindeutig sein müssen. In der folgenden Tabelle werden die verschiedenen Facility Felder beschrieben.
  
|Einrichtung|Beschreibung|
|:-----|:-----|
|FACILITY_NULL  <br/> |Für umfassend anwendbaren allgemeine Statuscodes wie S_OK oder E_OUTOF_MEMORY; der Wert ist NULL.  <br/> |
|FACILITY_ITF  <br/> |Für die meisten Statuscodes von Schnittstellenmethoden zurückgegeben; der Wert wird von der Benutzeroberfläche definiert. D. h., möglicherweise zwei HRESULT-Werte mit genau die gleiche 32-Bit-Wert zurückgegeben von zwei verschiedenen Schnittstellen verschiedene Bedeutungen haben.  <br/> |
|FACILITY_DISPATCH  <br/> |Für späte Bindung [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) -Schnittstelle Fehler.  <br/> |
|FACILITY_RPC  <br/> |Für Statuscodes von Remoteprozeduraufrufe zurückgegeben.  <br/> |
|FACILITY_STORAGE  <br/> |Für Statuscodes [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) oder [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) Aufrufe von Methoden für strukturierte Speicher zurückgegeben. Statuscodes Code (unteren 16 Bit) Werte im Bereich von Windows-Fehlercodes (d. h., kleiner als 256) haben dieselbe Bedeutung wie die entsprechende Windows-Fehler.  <br/> |
   
Das Feld ist eine eindeutige Zahl, die zum Darstellen der Fehlermeldung oder einer Warnung zugewiesen ist.
  

