---
title: Erweitern der Wetterleiste in Outlook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b355b98-dd7d-4f16-8257-367e5dd61b34
description: Hier erhalten Sie Informationen zum Integrieren eines Wetterwebdiensts eines Drittanbieters in die Wetterleiste in Outlook 2013, um Wetterbedingungen für einen vom Benutzer ausgewählten Ort bereitzustellen.
ms.openlocfilehash: 6b2462615813b056ec09168ab512d456e1a7bdd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796100"
---
# <a name="extending-the-weather-bar-in-outlook"></a>Erweitern der Wetterleiste in Outlook

Hier erhalten Sie Informationen zum Integrieren eines Wetterwebdiensts eines Drittanbieters in die Wetterleiste in Outlook 2013, um Wetterbedingungen für einen vom Benutzer ausgewählten Ort bereitzustellen.
  
## <a name="weather-bar-overview"></a>Übersicht über die Wetterleiste
<a name="ol15_weatherbar_overview"> </a>

In der Wetterleiste in Outlook werden die Wetterbedingungen und die Wettervorhersage für einen geografischen Standort angezeigt. Ein Benutzer kann einen oder mehrere Orte auswählen und Wetterdaten in der Wetterleiste im Kalendermodul sehen. Abbildung 1 zeigt die Wetterleiste mit einer 3-tägigen Wettervorhersage für New York, NY. 
  
**Abbildung 1. Wetterleiste in Outlook**

![Wetterleiste mit Vorhersage für New York.](media/ol15_WeatherBar_fig1.jpg)
  
Einstellungen für die Wetterleiste werden mit dem Benutzerprofil gespeichert. Je nach Outlook-Kontotyp wechselt die Einstellung, wie im Falle von Exchange-Konten, möglicherweise mit dem Benutzer auf allen Computern, auf denen er sich mit demselben Profil anmeldet. Alternativ kann der Benutzer die Einstellungen, wie im Falle von IMAP-/POP-Konten, auf jedem Computer anpassen.
  
Standardmäßig verwendet Outlook die von MSN Wetter bereitgestellten Wetterdaten. Die Wetterleiste unterstützt Wetterdaten von Drittanbieterwetterdiensten, die über ein definiertes Protokoll mit Outlook kommunizieren. Solange ein Drittanbieterwetterdienst dieses Protokoll unterstützt, können Benutzer die Wetterdaten von diesem Dienst in der Wetterleiste verwenden. In diesem Artikel wird das Protokoll für Drittanbieterwetterdienste für die Integration in die Wetterleiste in Outlook beschrieben.
  
## <a name="weather-bar-protocol"></a>Wetterleistenprotokoll
<a name="ol15_weatherbar_theprotocol"> </a>

Der Benutzer kann einen anderen Wetterdienst für die Wetterleiste angeben. Dieser muss allerdings das folgende Protokoll für die Kommunikation mit Outlook unterstützen.
  
1. Der Wetterdienst unterstützt eine Basis-URL zu einem Webdienst. Ein Contoso-Wetterwebdienst beispielsweise kann die Basis-URL http://service.contoso.com/data.aspx haben.
    
2. Mit dem Webdienst können die folgenden Parameter in Outlook an die Basis-URL angefügt werden, um einen Ortscode anzufordern: 
    
   - outputview = search: Dieser Parameter gibt an, dass es sich bei der Anforderung um eine Standortsuche handelt.
    
   - weasearchstr= _city_: Dieser Parameter gibt den Standort, also die _Stadt_ an, für die der Benutzer eine Wettervorhersage wünscht (z. B. London).
    
   - culture= _LCID_: Dieser Parameter gibt die Kultur der für den Benutzer auf diesem Computer installierten Office-Version an. Der LCID-Wert ist in [[RFC4646]-Tags für die Identifizierung von Sprachen](http://www.ietf.org/rfc/rfc4646.txt) definiert.
    
   - src=outlook: Dieser Parameter gibt an, dass Outlook die Clientanwendung ist, die den Dienst anfordert.
    
   Mit diesen Parametern kann Outlook den vom Benutzer gewünschten Ort verwenden und, wie vom Wetterdienst unterstützt, nach dem dazugehörigen Ortscode suchen. Der Wetterdienst sendet dann als Antwort an Outlook einen Ortscode im XML-Format, der dem [Outlook Weather Location XML Schema](outlook-weather-location-xml-schema.md) folgt. Abbildung 2 fasst die Webdienstanforderung und den darauf zurückgegebenen Ortscode zusammen.
    
   **Abbildung 2. Webdienstanforderung und der darauf zurückgegebene Ortscode**

   ![Anforderung und Antwort zum Wetterstandort](media/ol15_WeatherBar_Fig02.gif)
  
3. Mit dem Webdienst kann Outlook zudem die folgenden Parameter anfügen, um Vorhersageinformationen für einen Ortscode anzufordern:
    
   - wealocations= _code_: _code_ steht in diesem Parameter für einen Ortscode, den Outlook in Schritt 2 abruft, und der dem vom Benutzer gewünschten Ort zugeordnet wird. 
    
   - weadegreetype= _degreetype_: Dieser Parameter gibt an, ob das metrische oder imperiale Maßsystem für Temperatur verwendet wird. Geben Sie c für Metrisch oder f für Imperial unter _Degreetype_ ein. Dieser Parameter ist optional und ist nicht immer in der Webserviceanfrage vorhanden.
    
   - culture= _LCID_: Dieser Parameter gibt die Kultur der für den Benutzer auf diesem Computer installierten Office-Version an. Der LCID-Wert ist in [[RFC4646]-Tags für die Identifizierung von Sprachen](http://www.ietf.org/rfc/rfc4646.txt) definiert.
    
   - src=outlook: Dieser Parameter gibt an, dass Outlook die Clientanwendung ist, die den Dienst anfordert.
    
   Diese Parameter ermöglichen Outlook die Verwendung des im Schritt 2 zurückgegebenen Ortscodes und fordern Webdienstdaten für die Wettervorhersage an. Der Webdienst sollte eine Antwort an Outlook mit den entsprechenden Wetterdaten in XML senden, die das [Outlook Weather Information XML Schema](outlook-weather-information-xml-schema.md) befolgen. In Abbildung 3 ist die Webdienstanforderung und die Antwort mit Wetterinformationen für einen bestimmten Ortscode dargestellt.
    
   **Abbildung 3. Webdienstanforderung und Antwort mit Wetterinformationen**

   ![Anforderung von Wetterinformationen und entsprechende Antwort](media/ol15_WeatherBar_Fig03.gif)
  
## <a name="setting-the-weather-bar-to-use-a-weather-service"></a>Festlegen eines in der Wetterleiste zu verwendenden Wetterdiensts
<a name="ol15_weatherbar_setting"> </a>

Der Administrator oder der Hauptbenutzer können mit dem **WeatherServiceUrl**-Registrierungsschlüssel die Verwendung eines bestimmten Wetterdiensts in der Wetterleiste festlegen. Wenn die Basis-URL für einen Contoso-Wetterdienst beispielsweise http://service.contoso.com/data.aspx lautet, können Sie den **WeatherServiceUrl**-Schlüssel auf diese URL festlegen. 
  
In der folgenden Tabelle wird der **WeatherServiceUrl**-Schlüssel beschrieben. 
  
|||
|:-----|:-----|
|**Schlüssel** <br/> |HKCU\Software\Microsoft\Office\15.0\Outlook\Options\Calendar  <br/> |
|**Wertname** <br/> |**WeatherServiceUrl** <br/> |
|**Werttyp** <br/> |REG_SZ  <br/> |
|**Standardwert** <br/> |EMPTY_STRING  <br/> |
|**Beschreibung** <br/> |URL zu einem Wetterdatendienst  <br/> |
   
## <a name="dependent-conditions"></a>Abhängige Bedingungen
<a name="ol15_weatherbar_dependentconditions"> </a>

Outlook 2013 zeigt standardmäßig die Wetterleiste an. In diesem Abschnitt werden einige Gründe für das Nichtanzeigen der Wetterleiste aufgeführt.
  
### <a name="weather-bar-is-disabled"></a>Wetterleiste ist deaktiviert.

Überprüfen Sie zunächst dass **Wetter im Kalender anzeigen** auf der Registerkarte **Kalender** im Dialogfeld **Outlook-Optionen** ausgewählt ist. 
  
Beachten Sie, dass ein Administrator mithilfe der Gruppenrichtlinie die Wetterleiste in Outlook 2013 deaktivieren kann.
  
|||
|:-----|:-----|
|**Schlüssel** <br/> |HKCU\Software\Microsoft\Office\15.0\Outlook\Options\Calendar  <br/> |
|**Wertname** <br/> |**DisableWeather** <br/> |
|**Werttyp** <br/> |REG_DWORD  <br/> |
|**Standardwert** <br/> |0  <br/> |
|**Beschreibung** <br/> |Mit dem Wert 0 wird die Wetterleiste aktiviert; mit jedem anderen Wert wird die Wetterleiste deaktiviert.  <br/> |
   
Wenn die Wetterleiste mithilfe der Gruppenrichtlinie deaktiviert wurde, wird auf der Registerkarte **Kalender** das Kontrollkästchen **Wetter im Kalender anzeigen** nicht angezeigt. Wenden Sie sich an den Administrator, um die Wetterleiste wieder zu aktivieren. 
  
### <a name="office-is-disconnected-from-the-internet"></a>Office ist nicht mit dem Internet verbunden.

Stellen Sie sicher, dass Office eine Verbindung mit dem Internet herstellen kann. Wechseln Sie hierzu zur Registerkarte **Datenschutzoptionen** vom **Trust Center** in der Backstage-Ansicht, und vergewissern Sie sich, dass die Option **Internetverbindungen für Office zulassen** ausgewählt ist. 
  
Die Wetterleiste ist ebenfalls deaktiviert, wenn der Benutzer keine Updates für Office erhält.
  
Ein Administrator kann auch mithilfe der Gruppenrichtlinie den gesamten Onlineinhalt einschließlich Wetterleiste deaktivieren, indem er den folgenden Schlüssel in der Windows-Registrierung festlegt:
  
|||
|:-----|:-----|
|**Schlüssel** <br/> |HKCU\Software\Microsoft\Office\15.0\Common\Internet  <br/> |
|**Wertname** <br/> |**UseOnlineContent** <br/> |
|**Werttyp** <br/> |REG_DWORD  <br/> |
|**Standardwert** <br/> |2  <br/> |
|**Beschreibung** <br/> |Mit dem Wert 2 wird die Wetterleiste aktiviert; mit jedem anderen Wert wird die Wetterleiste deaktiviert.  <br/> |
   
Wenn die Wetterleiste mithilfe der Gruppenrichtlinie deaktiviert wurde, wird auf der Registerkarte **Kalender** das Kontrollkästchen **Wetter im Kalender anzeigen** nicht angezeigt. Wenden Sie sich an den Administrator, um die Wetterleiste wieder zu aktivieren. 
  
## <a name="weather-bar-example"></a>Beispiel einer Wetterleiste
<a name="ol15_weatherbar_example"> </a>

In diesem Abschnitt wird ein Beispiel eines Contoso-Wetterdiensts aufgeführt, der das vorherige Protokoll für die Kommunikation mit Outlook verwendet. Outlook ruft für jeden vom Benutzer ausgewählten Ort zunächst einen Ortscode von Contoso Wetter ab, und ruft anschließend unter Verwendung dieses Ortscodes den Contoso-Wetterdienst auf, um die Wetterdaten abzurufen.
  
### <a name="base-url"></a>Basis-URL

Contoso Wetter bietet die folgende Basis-URL für den Wetterdatendienst:
  
http://service.contoso.com/data.aspx
  
### <a name="getting-a-location-code"></a>Abrufen eines Ortscodes

Outlook fügt die oben in Schritt 2 beschriebenen Parameter an die Basis-URL an, um den Ortscode für einen geografischen Standort  _Ort_ abzurufen:
  
http://service.contoso.com/data.aspx?outputview=search&amp;weasearchstr= _Ort_
  
Beispiel: Wenn der BenutzerTokio in der Wetterleiste ausgewählt hat, verwendet Outlook die folgende URL zum Abrufen des Ortscodes für Tokio von Contoso Wetter: 
  
http://weather.service.contoso.com/data.aspx?outputview=search&amp;weasearchstr=tokyo
  
Contoso Wetter sendet die folgenden XML-Daten als Antwort zum Bereitstellen des Ortscodes für Tokio. Die XML-Daten entsprechen dem Outlook Weather Location XML-Schema. Beachten Sie, dass Wetterdienste in der Regel Daten für mehrere Orte zurückgeben (z. B. wenn der ausgewählte Ort eine Metropolregion ist). In diesem Beispiel umfasst die Antwort für Tokio zwei Orte, wobei jeder vom [weather](weather-element-weatherdata-elementoutlook-weather-location-schema.md)-Element eingeschlossen ist. Die entsprechenden Ortscodes lauten wie folgt: 
  
- wc:JAXX0085 für das **weatherlocationname**-Attribut  `Tokyo, JPN`
    
- wc:10038604 für das **weatherlocationname**-Attribut  `Shinjuku-ku, Tokyo, Japan`
    
```XML
<?xml version="1.0" ?>
<weatherdata>
  <weather weatherlocationcode="wc:JAXX0085" 
    weatherlocationname="Tokyo, JPN">
  </weather>
  <weather weatherlocationcode="wc:10038604" 
    weatherlocationname="Shinjuku-ku, JPN">
  </weather>
</weatherdata>

```

### <a name="getting-weather-information-for-a-location-code"></a>Abrufen von Wetterinformationen für einen Ortscode

Nach Abrufen des Ortscodes für einen Standort fügt Outlook die oben in Schritt 3 beschriebenen Parameter an die Basis-URL an, um die Wetterinformationen für diesen Ortscode abzurufen.
  
http://service.contoso.com/data.aspx?wealocations= _Code_
  
Beispiel: Wenn Outlook den Ortscode wc:JAXX0085 von Contoso Wetter für Tokio abgerufen hat, verwendet Outlook diesen Ortscode in der folgenden URL, um die Wetterinformationen abzurufen.
  
http://service.contoso.com/data.aspx?wealocations=wc:JAXX0085
  
Contoso Wetter sendet als Antwort die folgenden XML-Daten, um die Wetterinformationen für den Ortscode für Tokio bereitzustellen. Die XML-Daten folgen dem Outlook Weather Information XML-Schema.
  
```XML
<?xml version="1.0"?>
<weatherdata>
  <weather timezone="9" attribution="Data provided by Trey Research" 
    degreetype="F" imagerelativeurl="http://contoso.com/images/en-us/" 
    url="http://contoso.com/weather.aspx?eid=33568&amp;q=Tokyo-JPN" 
    weatherlocationname="Tokyo, JPN" 
    weatherlocationcode="wc:JAXX0085">
      <current winddisplay="9 mph NNW" windspeed="9" humidity="90" feelslike="44" 
        observationpoint="Tokyo" observationtime="06:00:00" 
        shortday="Sat" day="Saturday" date="2012-04-14" skytext="Rain" skycode="11" 
        temperature="48"/>
      <forecast shortday="Sat" day="Saturday" date="2012-04-14" precip="95" skytextday="Rain"
        skycodeday="11" high="55" low="47"/>
      <forecast shortday="Sun" day="Sunday" date="2012-04-15" precip="5" skytextday="Partly Cloudy" 
        skycodeday="30" high="65" low="43"/>
      <forecast shortday="Mon" day="Monday" date="2012-04-16" precip="5" skytextday="Partly Cloudy" 
        skycodeday="30" high="64" low="52"/>
      <forecast shortday="Tue" day="Tuesday" date="2012-04-17" precip="70" skytextday="Showers / Clear" 
        skycodeday="39" high="66" low="53"/>
      <forecast shortday="Wed" day="Wednesday" date="2012-04-18" precip="55" skytextday="Showers / Clear" 
        skycodeday="39" high="68" low="51"/>
  </weather>
</weatherdata>

```

### <a name="resetting-outlook-to-use-msn-weather"></a>Zurücksetzen von Outlook zum Verwenden von MSN Wetter

Auch wenn Outlook standardmäßig MSN Wetter verwendet, kann der Benutzer, nachdem er einen anderen Wetterdienst für die Wetterleiste ausgewählt hat, den **WeatherServiceUrl**-Schlüssel in der Windows-Registrierung löschen, um MSN Wetter erneut zu verwenden. Durch Löschen dieses Registrierungsschlüssel wird Outlook zum Verwenden von MSN Wetter zurückgesetzt. 
  
## <a name="conclusion"></a>Schlussbemerkung
<a name="ol15_weatherbar_conclusion"> </a>

Die Wetterleiste im Outlook-Kalender verwendet standardmäßig MSN Wetter für die Bereitstellung der Wettervorhersage für einen bestimmten Ort. Benutzer können Wetterinformationen für die gewünschten Orte sehen. Drittanbieter-Wetterdatendienste können auch in die Wetterleiste integriert werden, wenn Sie das Outlook Weather Location XML-Schema und das Outlook Weather Information XML-Schema unterstützen, und einen einfachen Webdienstprotokoll für die Kommunikation mit Outlook befolgen.
  
## <a name="see-also"></a>Siehe auch

- [XML-Schema für Wetterstandort in Outlook](outlook-weather-location-xml-schema.md)   
- [Outlook Weather Information XML Schema](outlook-weather-information-xml-schema.md)
    

