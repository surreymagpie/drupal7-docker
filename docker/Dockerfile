# Creates an image with all dependencies for drupal 7 website
# - Apache 2.4
# - PHP 7.2 with GD, curl, mbstring, uploadprogress

FROM ubuntu:18.04

LABEL maintainer="surreymagpie@yahoo.co.uk"

#set timezone and locale
RUN ln -snf /usr/share/zoneinfo/Europe/London /etc/localtime && \
    apt-get update && apt-get install -yqq \
    	locales \
    	tzdata && \
	locale-gen en_GB.utf8 && \
    apt-get clean && apt-get autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Install generic utilities
RUN apt-get -yqq update && \
	apt-get -yqq install \
		git \
		curl \
		wget \
		zip \
		unzip && \
    apt-get clean && apt-get autoremove && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
