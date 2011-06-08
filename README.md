Authors:
 - javiacei
 - cordoval
 - Moisés Maciá

Changelog:
 - Added dependency to DoctrineExtensions\Paginate to handle proper pagination (see https://github.com/beberlei/DoctrineExtensions)
 - Added support to paginate multiple lists at once
 - Changed the Paginador class name to Paginator
   this is how services.xml defines our service, with a parameter set to the class implementing pagination and passing a service id
 
       <parameters>
           <parameter key="simple_paginador.class">Ideup\SimplePaginatorBundle\Paginator\Paginator</parameter>
       </parameters>
 
       <services>
           <service id="ideup.simple_paginator" class="%simple_paginator.class%">
               <argument type="service" id="request" strict="false" />
           </service>
       </services>
 
 - implemented Twig extension and calling the Class Paginator from there

TODO:
  1 - Testing it with a hello world sample
  2 - Making it work with a more generic Doctrine Collections

