---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f58d0f5cd7dfe74d3859d4f06a41aad6c3a55ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792582"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**Betrifft**: Outlook 
  
Konfiguriert einen Message-Dienst neu.
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Parameter

 _lpUID_
  
> [in] Ein Zeiger auf die [MAPIUID](mapiuid.md) -Struktur, die den eindeutigen Bezeichner für den Dienst so konfigurieren Sie enthält. 
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster im Eigenschaftsfenster Konfiguration.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die die Anzeige des Eigenschaftenfensters steuert. Die folgenden Kennzeichen können festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
MSG_SERVICE_UI_READ_ONLY 
  
> Der Nachrichtendienst sollte das Eigenschaftenfenster Konfiguration anzuzeigen, aber nicht ermöglichen Benutzern das ändern. Die meisten Message Dienste ignoriert dieses Flag.
    
SERVICE_UI_ALLOWED 
  
> Der Nachrichtendienst sollte das Eigenschaftenblatt Konfiguration angezeigt werden nur, wenn der Dienst nicht vollständig konfiguriert ist.
    
SERVICE_UI_ALWAYS 
  
> Message-Dienst muss immer das Eigenschaftenblatt Konfiguration anzeigen. Wenn SERVICE_UI_ALWAYS nicht festgelegt ist, kann ein Eigenschaftenblatt Konfiguration weiterhin angezeigt, wenn SERVICE_UI_ALLOWED festgelegt ist und gültige Konfigurationsinformationen nicht verfügbar aus Array-Eigenschaft den Wert im _LpProps_ -Parameter ist. SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS muss für ein Eigenschaftenfenster, angezeigt werden soll, festgelegt werden. 
    
 _cValues_
  
> [in] Die Anzahl der Eigenschaftswerte in der Struktur [SPropValue](spropvalue.md) auf _LpProps_zeigt. 
    
 _lpProps_
  
> [in] Ein Zeiger auf ein Array der Eigenschaftswerte, die beschreiben, die Eigenschaften im Eigenschaftenfenster angezeigt. Der Parameter _LpProps_ darf nicht NULL sein, wenn der Nachrichtendienst ohne Benutzeroberfläche konfiguriert werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Nachrichtendienst wurde erfolgreich konfiguriert.
    
MAPI_E_EXTENDED_ERROR 
  
> Fehler, die speziell für eine Message Service. Wenn die Struktur [MAPIERROR](mapierror.md) erhalten möchten, die den Fehler beschreibt, sollte die Client-Anwendung die [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) -Methode aufrufen. 
    
MAPI_E_NOT_FOUND 
  
> Die auf den _LpUID_ **MAPIUID** stimmt nicht überein, die einem vorhandenen Meldung-Dienst. 
    
MAPI_E_NOT_INITIALIZED 
  
> Message-Dienst hat keine Funktion bei Einstiegspunkt.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im Eigenschaftenfenster abgebrochen. 
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::ConfigureMsgService** -Methode ermöglicht eine Message Service mit oder ohne ein Eigenschaftenblatt Konfiguration konfiguriert werden soll. 
  
Um ohne Eigenschaft Blatt Bildschirm Konfiguration zu ermöglichen, Vorbereiten Message-Dienste in der Regel eine Headerdatei, die Konstanten für alle erforderlichen und optionalen Eigenschaften und deren Werte enthält.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie die **MAPIUID** -Struktur für den Dienst so konfigurieren abgerufen Sie die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Spalte aus der Nachrichtendienst Zeile in der Tabelle der Dienste. Weitere Informationen finden Sie unter dem Verfahren in der [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Methode. 
  
Sie können eine Message Service konfigurieren, ohne ein Eigenschaftenfenster, die einem Benutzer, nur, wenn Sie Advance Informationen über die Eigenschaftswerte festgelegt werden soll. Wenn Sie einen Nachrichtendienst ohne ein Eigenschaftenblatt konfigurieren, valid-Eigenschaftswerte im _LpProps_ -Parameter übergeben, und die Kennzeichen MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS nicht festlegen. 
  
Wenn Sie von der Benutzer über ein Eigenschaftenblatt aller oder einiger der Konfigurationsinformationen erhalten haben, legen Sie SERVICE_UI_ALLOWED in _UlFlags_. Wenn Sie vorhandene Eigenschafteninformationen nur für die Standardeinstellungen einrichten und der Benutzer die Einstellungen zu ändern kann, legen Sie SERVICE_UI_ALWAYS in _UlFlags_.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI (engl.) verwendet die **IMsgServiceAdmin::ConfigureMsgService** -Methode, um einen Dienst zu konfigurieren, der zu einem Profil hinzugefügt wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

