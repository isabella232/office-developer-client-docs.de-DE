---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432380"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine vom Profil-Assistenten aufgerufene Rückruffunktion, damit ein Dienstanbieter auf Benutzerereignisse reagieren kann, wenn die Eigenschaftenblätter oder Seiten des Anbieters angezeigt werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI-Profil-Assistent  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

_hDlg_
  
> in Fensterhandle für das Dialogfeld Profil-Assistent. 
    
_wMsgID_
  
> in Die zu verarbeitende Fenstermeldung. Zusätzlich zu den von einem modalen Dialogfeld erwarteten regulären Fenster Meldungen können die folgenden Nachrichten empfangen werden:
    
WM_CLOSE 
  
> Der Profil-Assistent wurde abgeschlossen. Der Dienstanbieter muss alle erforderlichen Aufräumarbeiten ausführen, beispielsweise die dezuweisung dynamisch zugewiesener Arbeitsspeicher. 
    
WM_COMMAND 
  
> Eines der Steuerelemente des Anbieters wurde ausgewählt, oder auf die Schaltfläche **weiter** oder **zurück** wurde geklickt. Der Wert im Parameter _wParam_ gibt an, welches dieser Benutzerereignisse aufgetreten ist. 
    
WM_INITDIALOG 
  
> Der Benutzer ist zu einer anderen Eigenschaftenseite gewechselt, für die das Dialogfeld initialisiert werden muss. Der Anbieter sollte die Steuerelemente initialisieren, die der Profil-Assistent dem Dialogfeld hinzugefügt hat. 
    
WIZ_QUERYNUMPAGES 
  
> Der Profil-Assistent fordert die Anzahl der Seiten an, die vom Anbieter angezeigt werden müssen. Der Anbieter sollte die Anzahl der Seiten anstelle von TRUE oder FALSE zurückgeben. Verwenden Sie beispielsweise die folgende Return-Anweisung, um anzugeben, dass drei Seiten angezeigt werden sollen:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> in Ein 32-Bit-Parameter, der Fenster Meldungen zugeordnet ist. Mögliche Werte hängen von der im Parameter _wMsgID_ angegebenen Meldung ab. Zusätzlich zu den erwarteten Werten mit den regulären Fenster Meldungen für ein modales Dialogfeld können die folgenden Werte empfangen werden: 
    
WIZ_NEXT 
  
> Wenn _WMSGID_ WM_COMMAND enthält, hat der Benutzer auf die Schaltfläche **weiter** geklickt. 
    
WIZ_PREV 
  
> Wenn _WMSGID_ WM_COMMAND enthält, hat der Benutzer auf die Schaltfläche " **zurück** " geklickt. 
    
_lParam_
  
> in Ein 32-Bit-Parameter, der Fenster Meldungen zugeordnet ist. Mögliche Werte hängen von der im Parameter _wMsgID_ angegebenen Meldung ab. 
    
## <a name="return-value"></a>Rückgabewert

Der von einer **SERVICEWIZARDDLGPROC** -basierten Funktion zurückgegebene Wert ist von der empfangenen Fenster Nachricht abhängig. Beachten Sie insbesondere den außergewöhnlichen Rückgabewert für die WIZ_QUERYNUMPAGES-Nachricht. Die normalen Rückgabewerte sind: 
  
TRUE 
  
> Der Dienstanbieter hat die empfangene Fenstermeldung verarbeitet. 
    
FALSE 
  
> Der Dienstanbieter hat die empfangene Fenstermeldung nicht verarbeitet.
    
## <a name="remarks"></a>Bemerkungen

Wenn der Benutzer von einer Eigenschaftenseite zu einer anderen wechselt, ist der Anbieter dafür verantwortlich, die Steuerelemente der alten Seite zu verbergen und die Steuerelemente für die nächste oder vorherige Seite anzuzeigen. Wenn der Benutzer auf die Schaltfläche **weiter** klickt, wird die **SERVICEWIZARDDLGPROC** -basierte Funktion mit der WM_COMMAND-Nachricht und WIZ_NEXT im _wParam_ -Parameter aufgerufen. In den folgenden Schritten wird beschrieben, was zwischen dem Zeitpunkt, zu dem der Benutzer auf **Next** klickt, und dem Zeitpunkt, zu dem die Konfigurationsseiten des ersten Anbieters gerendert werden. 
  
1. Der Profil-Assistent blendet alle Steuerelemente aus dem Fenster aus. 
    
2. Der Profil-Assistent fügt der Seite die ausgeblendeten Steuerelemente des Anbieters hinzu. 
    
3. Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC**auf und sendet die WM_INITDIALOG-Nachricht, sodass der Anbieter die Steuerelemente initialisieren kann. 
    
4. Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC**auf und sendet die WIZ_QUERYNUMPAGES-Nachricht. Der Anbieter gibt die Anzahl der Seiten zurück, die angezeigt werden sollen. 
    
5. Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC**auf und sendet die WM_COMMAND-Nachricht mit dem _wParam_ -Parameter, der auf WIZ_NEXT oder WIZ_PREV festgelegt ist. Zu diesem Zeitpunkt gibt der Anbieter entweder FALSE {Error} zurück oder zeigt seine Steuerelemente an und gibt TRUE {Success} zurück. Wenn der Profil-Assistent ID_NEXT übergibt, wird die erste Seite des Anbieters angezeigt. Wenn ID_PREV übergeben wird, wird die letzte Seite angezeigt. 
    
6. Der Profil-Assistent ruft die **SERVICEWIZARDDLGPROC** -Funktion des Anbieters auf und sendet die WM_COMMAND-Nachricht mit dem _wParam_ -Parameter, der auf WIZ_NEXT oder WIZ_PREV festgelegt ist (abhängig von der Schaltfläche, auf die der Benutzer geklickt hat). Der Anbieter ist dafür verantwortlich, seine Steuerelemente anzuzeigen oder zu verbergen und seine Daten in die **IMAPIProp** zu schreiben, die an den Profil-Assistenten übergeben wurden, um die Reihenfolge der Seiten zu durchlaufen. Der Anbieter sollte TRUE zurückgeben, wenn die nächste oder die vorherige Seite erfolgreich angezeigt wurde, und FALSE, wenn weder die nächste noch die vorherige Seite angezeigt werden konnte. Der Anbieter muss sich dessen klar sein, wenn er sich außerhalb seiner Seitenfolge befindet, und entsprechend reagieren, indem er seine Steuerelemente versteckt und seine Daten in das Profil schreibt. 
    
7. Wenn der Benutzer außerhalb des Seiten Angebots des Anbieters ausgeführt wird, löscht der Profil-Assistent die ausgeblendeten Steuerelemente des Anbieters aus dem Dialogfeld und ruft den nächsten Anbieter auf oder zeigt die nächste Seite an, wenn dies der letzte Anbieter war. 
    

