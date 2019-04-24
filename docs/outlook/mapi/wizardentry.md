---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329554"
---
# <a name="wizardentry"></a>WIZARDENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Dienstanbieter-Einstiegspunktfunktion, die vom Profil-Assistenten aufgerufen wird, um genügend Informationen zum Anzeigen der Konfigurationseigenschaften Blätter des Anbieters abzurufen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI-Profil-Assistent  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a>Parameter

 _hProviderDLLInstance_
  
> in Instanz-Handle der DLL des Dienstanbieters. 
    
 _lpcsResourceName_
  
> Out Zeiger auf eine Zeichenfolge, die den vollständigen Namen der Dialogfeldressource enthält, die während der Konfiguration vom Profil-Assistenten angezeigt werden soll. Die maximale Größe der Zeichenfolge, einschließlich des NULL-Terminators, beträgt 32 Zeichen. 
    
 _lppDlgProc_
  
> Out Zeiger auf eine Windows-Standarddialogfeld-Prozedur, die vom Profil-Assistenten aufgerufen wird, um den Anbieter über verschiedene Ereignisse zu informieren. 
    
 _lpMAPIProp_
  
> in Zeiger auf eine Implementierung der Eigenschaften Schnittstelle, die Zugriff auf die Konfigurationseigenschaften bereitstellt. 
    
 _lpMapiSupportObject_
  
> in Zeiger auf das MAPI-Unterstützungsobjekt, das für diese Sitzung gilt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die **WIZARDENTRY** -Funktion des Dienstanbieters wurde erfolgreich aufgerufen. 
    
MAPI_E_CALL_FAILED 
  
> Der Vorgang konnte nicht abgeschlossen werden.
    
## <a name="remarks"></a>Bemerkungen

Der Profil-Assistent ruft die **WIZARDENTRY** -basierte Funktion auf, wenn Sie bereit ist, die Konfigurationsbenutzeroberfläche des Dienstanbieters anzuzeigen. Wenn der Profil-Assistent alle Anbieter konfiguriert hat, schreibt er die Konfigurationseigenschaften in das Profil durch Aufrufen von [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Der Name der **WIZARDENTRY** -basierten Funktion muss im WIZARD_ENTRY_NAME-Eintrag in MAPISVC. inf stehen. 
  
Der Ressourcenname ist der der Dialogfeldressource, die im Bereich des Profil-Assistenten gerendert wird. Die zurückgegebene Ressource muss alle Seiten in einer einzelnen Dialogfeldressource enthalten. Wenn der Profil-Assistent diese Ressource empfängt, ignoriert er die Dialog Formatvorlage, aber nicht die Steuerelementformat Vorlagen und erstellt alle Steuerelemente als untergeordnete Objekte der Seite des Profil-Assistenten. Alle Steuerelemente werden anfänglich ausgeblendet. Anbieter sollten sicherstellen, dass die Koordinaten für Ihre Steuerelemente NULL oder nullbasiert sind und nicht eine maximale Breite von 200 Dialogeinheiten und eine maximale Höhe von 150 Dialogeinheiten überschreiten. Steuerelement-IDs unter 400 sind für den Profil-Assistenten reserviert. Der Profil-Assistent zeigt den Titel des Anbieters fett formatiert über der Benutzeroberfläche des Anbieters an. 
  
Der im _lpMAPIProp_ -Parameter angegebene Eigenschaften Schnittstellenzeiger sollte vom Anbieter zur späteren Bezugnahme aufbewahrt werden. Der Profil-Assistent behandelt nur die grundlegendsten Eigenschaften, und der Anbieter kann die Eigenschaften Schnittstellenimplementierung verwenden, um zusätzliche Eigenschaften einzuschließen. Während der Konfiguration sollten Anbieter Ihre Konfigurationseigenschaften dem Objekt hinzufügen, das die Eigenschaften Schnittstelle implementiert. Nachdem alle Anbieter konfiguriert wurden, fügt der Profil-Assistent diese Eigenschaften dem Profil hinzu. 
  
Weitere Informationen zur Verwendung dieser Funktion finden Sie unter [unterstützen der Nachrichtendienst Konfiguration](supporting-message-service-configuration.md). 
  

