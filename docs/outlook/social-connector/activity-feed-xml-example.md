---
title: Beispiel für Aktivitätsfeed-XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge des Aktivitätsfeeds, die an den Outlook Social Connector (OSC) zurückgegeben wird, nachdem die ISocialSession2::GetActivitiesEx-Methode für ein soziales Netzwerk aufruft.
ms.openlocfilehash: bb8af45f25d8ee2897a3a01e2863466aeacec4e8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538326"
---
# <a name="activity-feed-xml-example"></a>Beispiel für Aktivitätsfeed-XML

Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge des Aktivitätsfeeds, die an den Outlook Social Connector (OSC) zurückgegeben wird, nachdem die [ISocialSession2::GetActivitiesEx-Methode](isocialsession2-getactivitiesex.md) für ein soziales Netzwerk aufruft. 
  
Das Beispiel zeigt die **activityFeed-XML,** die die folgenden vier Aktivitäten enthält, die jeweils durch das **activityDetails-Element** getrennt sind und eine Vorlage für Anzeigezwecke abgleichen: 
  
- Ein Profilbildupdate von Melissa Macbeth, deren **Besitzer-ID** im sozialen Netzwerk 4667647 ist. Diese Aktivität gibt drei Vorlagenvariablen vom Typ **publisherVariable**, **listVariable** und **pictureVariable** an (die in **listVariable eingeschlossen ist).** Diese Variablen geben die Person an, die das Aktivitätsfeedelement veröffentlicht hat, und Informationen für das zu aktualisierende Bild (unter Verwendung des Namens **,** **Werts,** **altText** und **href** untergeordneten Elemente von **pictureVariable**).
    
- Ein Profilbildupdate von Michael Affronti, dessen **BesitzerID** im sozialen Netzwerk 5015012 ist. Ähnlich wie bei der letzten Aktivität gibt diese Aktivität drei Vorlagenvariablen vom Typ **publisherVariable,** **listVariable** und **pictureVariable an.** Diese Variablen geben die Person an, die das Aktivitätsfeedelement veröffentlicht hat, und Informationen für das zu aktualisierende Bild.
    
- Ein Statusupdate von Michael Affronti, das die gleiche **Besitzer-ID** von 5015012 wie die letzte Aktivität zeigt. Diese Aktivität gibt zwei Vorlagenvariablen vom Typ **publisherVariable** und **textVariable an.** **publisherVariable** gibt die Person an, die das Aktivitätsfeedelement veröffentlicht hat, und **textVariable** enthält einen **Wert** der Statuszeile.  `is hiking on Mount Rainier this weekend!`
    
- Ein Blogbeitrag von Michael Affronti mit der gleichen **Besitzer-ID** von 5015012 wie die letzten beiden Aktivitäten. Diese Aktivität gibt zwei Vorlagenvariablen vom Typ **publisherVariable** und **linkVariable an.** **publisherVariable** gibt die Person an, die das Aktivitätsfeedelement veröffentlicht hat, und  **linkVariable** enthält weitere Informationen (angegeben durch die untergeordneten Elemente **Name,** Text und Wert von **linkVariable**) zum Blogbeitrag.
    
Jede der vier Aktivitäten gibt einen **templateID-Wert** an, der einer der drei vorlagen entspricht, die durch das **Templates-Element angegeben** werden. Jede Vorlage befindet sich im eigenen **activityTemplateContainer-Element,** das durch einen **templateID-Wert** identifiziert wird, der auch zum Anzeigen einer Aktivität verwendet wird, die denselben **templateID-Wert** besitzt. 
  
Eine ausführliche Beschreibung der im Beispiel verwendeten XML-Elemente finden Sie in den folgenden Themen: 
  
- [Übersicht über XML für ein Aktivitätsfeedelement](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails-Element](activitydetails-element.md)
    
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)
    
- [Vorlagenvariablen](template-variables.md)
    
## <a name="xml-example"></a>XML-Beispiel

Das folgende Beispiel zeigt die **activityFeed-XML** von vier Aktivitäten: zwei Profilbildaktualisierungen, eine Statusaktualisierung und einen Blogbeitrag. Die XML gibt außerdem drei Aktivitätsanzeigevorlagen zum Anzeigen der entsprechenden Aktivitäten an. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <network>Contoso</network>
  <activities>
    <activityDetails>
      <ownerID>4667647</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a31</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-05T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>4667647</id>
          <nameHint>Melissa Macbeth</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a32</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-08T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a38</objectID>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <publishDate>2010-03-08T18:30:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com</profileUrl>
        </templateVariable>
        <templateVariable type="textVariable">
          <name>statusText</name>
          <value>is hiking on Mount Rainier this weekend!</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a39</objectID>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <publishDate>2010-03-04T15:00:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>https://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
  </activities>
  <templates>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <activityTemplate>
        <type>Photo</type>
        <title>{publisher:Publisher} has a new profile photo: </title>
        <data>{list:ProfilePhoto({picture:Photo})}</data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a>Siehe auch

- [OSC-Anbieter-XML-Beispiele](osc-provider-xml-examples.md)  
- [XML für Aktivitäten](xml-for-activities.md) 
- [Capabilities XML(Beispiel)](capabilities-xml-example.md)  
- [Friends-XML-Beispiel](friends-xml-example.md)
- [Outlook XML-Schema des Anbieters für sozialen Connector](outlook-social-connector-provider-xml-schema.md)

